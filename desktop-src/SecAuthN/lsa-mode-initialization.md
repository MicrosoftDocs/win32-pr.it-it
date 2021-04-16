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
# <a name="lsa-mode-initialization"></a>Inizializzazione della modalità LSA

All'avvio del sistema, l'autorità di [*sicurezza locale*](../secgloss/l-gly.md) (LSA) carica automaticamente tutte le dll [](../secgloss/s-gly.md)del / [*pacchetto di autenticazione*](../secgloss/a-gly.md) Security Support Provider (SSP/AP) registrate nello spazio di elaborazione. Nelle illustrazioni seguenti viene illustrato il processo di inizializzazione.

> [!Note]  
> "Kerberos" rappresenta Microsoft [*Kerberos*](../secgloss/k-gly.md) SSP/AP e "My SSP/AP" rappresenta un SSP/AP personalizzato che contiene due pacchetti di sicurezza personalizzati.

 

![inizializzazione della modalità LSA](images/lsamode1.png)

All'avvio, LSA chiama la funzione [**SpLsaModeInitialize**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-splsamodeinitializefn) in ogni SSP/AP per ottenere i puntatori alle funzioni implementate da ogni [*pacchetto di sicurezza*](../secgloss/s-gly.md) della dll. I puntatori a funzione vengono passati all'LSA in una matrice di strutture della [**\_ \_ tabella della funzione SECPKG**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_function_table) .

![LSA chiama splsamodeinitialize per ottenere i puntatori a funzione](images/lsamode2.png)

Dopo aver ricevuto il set di strutture della [**\_ \_ tabella di funzioni SECPKG**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_function_table) , LSA chiama ogni funzione [**SpInitialize**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spinitializefn) del pacchetto di sicurezza. LSA usa questa chiamata di funzione per passare ogni pacchetto di sicurezza una struttura della [**\_ tabella della \_ funzione \_ LSA SECPKG**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table) , che contiene i puntatori alle funzioni di supporto LSA disponibili per i pacchetti di sicurezza. Oltre a archiviare i puntatori alle funzioni di supporto LSA, i pacchetti di sicurezza personalizzati devono utilizzare la rispettiva implementazione della funzione **SpInitialize** per eseguire qualsiasi elaborazione correlata all'inizializzazione.

Per un elenco delle funzioni di supporto LSA disponibili per i pacchetti di sicurezza in modalità LSA, vedere [funzioni LSA chiamate da SSP/APS](authentication-functions.md).

Per informazioni sulla registrazione di una DLL SSP/AP, vedere la pagina relativa alla registrazione di DLL [SSP/AP](registering-ssp-ap-dlls.md).

 

 
