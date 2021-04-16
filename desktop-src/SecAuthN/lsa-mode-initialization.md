---
description: All'avvio del sistema, l'autorità di sicurezza locale (LSA) carica automaticamente tutte le dll del pacchetto di Security Support Provider/autenticazione (SSP/AP) registrate nello spazio di processo. Nelle illustrazioni seguenti viene illustrato il processo di inizializzazione.
ms.assetid: 2d52cbbf-9e28-4c6f-8b4c-448b73c6dbf8
title: Inizializzazione della modalità LSA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e4212a584d290e67c6465488c8398604db2c16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529742"
---
# <a name="lsa-mode-initialization"></a><span data-ttu-id="78ab7-104">Inizializzazione della modalità LSA</span><span class="sxs-lookup"><span data-stu-id="78ab7-104">LSA Mode Initialization</span></span>

<span data-ttu-id="78ab7-105">All'avvio del sistema, l'autorità di [*sicurezza locale*](../secgloss/l-gly.md) (LSA) carica automaticamente tutte le dll [](../secgloss/s-gly.md)del / [*pacchetto di autenticazione*](../secgloss/a-gly.md) Security Support Provider (SSP/AP) registrate nello spazio di elaborazione.</span><span class="sxs-lookup"><span data-stu-id="78ab7-105">When the computer system is started, the [*Local Security Authority*](../secgloss/l-gly.md) (LSA) automatically loads all registered [*security support provider*](../secgloss/s-gly.md)/[*authentication package*](../secgloss/a-gly.md) (SSP/AP) DLLs into its process space.</span></span> <span data-ttu-id="78ab7-106">Nelle illustrazioni seguenti viene illustrato il processo di inizializzazione.</span><span class="sxs-lookup"><span data-stu-id="78ab7-106">The following illustrations show the initialization process.</span></span>

> [!Note]  
> <span data-ttu-id="78ab7-107">"Kerberos" rappresenta Microsoft [*Kerberos*](../secgloss/k-gly.md) SSP/AP e "My SSP/AP" rappresenta un SSP/AP personalizzato che contiene due pacchetti di sicurezza personalizzati.</span><span class="sxs-lookup"><span data-stu-id="78ab7-107">"Kerberos" represents the Microsoft [*Kerberos*](../secgloss/k-gly.md) SSP/AP, and "My SSP/AP" represents a custom SSP/AP that contains two custom security packages.</span></span>

 

![inizializzazione della modalità LSA](images/lsamode1.png)

<span data-ttu-id="78ab7-109">All'avvio, LSA chiama la funzione [**SpLsaModeInitialize**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-splsamodeinitializefn) in ogni SSP/AP per ottenere i puntatori alle funzioni implementate da ogni [*pacchetto di sicurezza*](../secgloss/s-gly.md) della dll.</span><span class="sxs-lookup"><span data-stu-id="78ab7-109">At startup, the LSA calls the [**SpLsaModeInitialize**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-splsamodeinitializefn) function in each SSP/AP to obtain pointers to the functions implemented by each [*security package*](../secgloss/s-gly.md) in the DLL.</span></span> <span data-ttu-id="78ab7-110">I puntatori a funzione vengono passati all'LSA in una matrice di strutture della [**\_ \_ tabella della funzione SECPKG**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_function_table) .</span><span class="sxs-lookup"><span data-stu-id="78ab7-110">The function pointers are passed to the LSA in an array of [**SECPKG\_FUNCTION\_TABLE**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_function_table) structures.</span></span>

![LSA chiama splsamodeinitialize per ottenere i puntatori a funzione](images/lsamode2.png)

<span data-ttu-id="78ab7-112">Dopo aver ricevuto il set di strutture della [**\_ \_ tabella di funzioni SECPKG**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_function_table) , LSA chiama ogni funzione [**SpInitialize**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spinitializefn) del pacchetto di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="78ab7-112">After receiving the set of [**SECPKG\_FUNCTION\_TABLE**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_function_table) structures, the LSA calls each security package's [**SpInitialize**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spinitializefn) function.</span></span> <span data-ttu-id="78ab7-113">LSA usa questa chiamata di funzione per passare ogni pacchetto di sicurezza una struttura della [**\_ tabella della \_ funzione \_ LSA SECPKG**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table) , che contiene i puntatori alle funzioni di supporto LSA disponibili per i pacchetti di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="78ab7-113">The LSA uses this function call to pass each security package an [**LSA\_SECPKG\_FUNCTION\_TABLE**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table) structure, which contains pointers to the LSA support functions available to security packages.</span></span> <span data-ttu-id="78ab7-114">Oltre a archiviare i puntatori alle funzioni di supporto LSA, i pacchetti di sicurezza personalizzati devono utilizzare la rispettiva implementazione della funzione **SpInitialize** per eseguire qualsiasi elaborazione correlata all'inizializzazione.</span><span class="sxs-lookup"><span data-stu-id="78ab7-114">In addition to storing the pointers to the LSA support functions, custom security packages should use their implementation of the **SpInitialize** function to perform any initialization-related processing.</span></span>

<span data-ttu-id="78ab7-115">Per un elenco delle funzioni di supporto LSA disponibili per i pacchetti di sicurezza in modalità LSA, vedere [funzioni LSA chiamate da SSP/APS](authentication-functions.md).</span><span class="sxs-lookup"><span data-stu-id="78ab7-115">For a list of the LSA support functions available to LSA-mode security packages, see [LSA Functions Called by SSP/APs](authentication-functions.md).</span></span>

<span data-ttu-id="78ab7-116">Per informazioni sulla registrazione di una DLL SSP/AP, vedere la pagina relativa alla registrazione di DLL [SSP/AP](registering-ssp-ap-dlls.md).</span><span class="sxs-lookup"><span data-stu-id="78ab7-116">For information about registering an SSP/AP DLL, see [Registering SSP/AP DLLs](registering-ssp-ap-dlls.md).</span></span>

 

 
