---
description: Quando il sistema del computer viene avviato, l'autorità di sicurezza locale (LSA) carica automaticamente tutte le DLL del provider di supporto per la sicurezza/pacchetto di autenticazione (SSP/AP) registrate nello spazio di elaborazione. Le illustrazioni seguenti illustrano il processo di inizializzazione.
ms.assetid: 2d52cbbf-9e28-4c6f-8b4c-448b73c6dbf8
title: Inizializzazione in modalità LSA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff4c55397e5970b8401e1429eba7d92a034e76ce0c999950131167580ded7e5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118922131"
---
# <a name="lsa-mode-initialization"></a>Inizializzazione in modalità LSA

All'avvio del sistema [](../secgloss/l-gly.md) del computer, l'autorità di sicurezza locale (LSA) carica automaticamente tutte le DLL del pacchetto di autenticazione del [*provider*](../secgloss/s-gly.md)di supporto per la sicurezza / [](../secgloss/a-gly.md) (SSP/AP) registrate nello spazio di elaborazione. Le illustrazioni seguenti illustrano il processo di inizializzazione.

> [!Note]  
> "Kerberos" rappresenta microsoft [*Kerberos*](../secgloss/k-gly.md) SSP/AP e "My SSP/AP" rappresenta un SSP/AP personalizzato che contiene due pacchetti di sicurezza personalizzati.

 

![Inizializzazione in modalità lsa](images/lsamode1.png)

All'avvio, LSA chiama la funzione [**SpLsaModeInitialize**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-splsamodeinitializefn) in ogni provider di servizi [](../secgloss/s-gly.md) di configurazione/ap per ottenere puntatori alle funzioni implementate da ogni pacchetto di sicurezza nella DLL. I puntatori a funzione vengono passati all'LSA in una matrice di [**strutture SECPKG \_ FUNCTION \_ TABLE.**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_function_table)

![lsa chiama splsamodeinitialize per ottenere i puntatori a funzione](images/lsamode2.png)

Dopo aver ricevuto il set di [**strutture SECPKG \_ FUNCTION \_ TABLE,**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_function_table) l'LSA chiama la funzione [**SpInitialize**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spinitializefn) di ogni pacchetto di sicurezza. LSA usa questa chiamata di funzione per passare a ogni pacchetto di sicurezza una struttura [**LSA \_ SECPKG \_ FUNCTION \_ TABLE,**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table) che contiene puntatori alle funzioni di supporto LSA disponibili per i pacchetti di sicurezza. Oltre a archiviare i puntatori alle funzioni di supporto LSA, i pacchetti di sicurezza personalizzati devono usare la relativa implementazione della **funzione SpInitialize** per eseguire qualsiasi elaborazione correlata all'inizializzazione.

Per un elenco delle funzioni di supporto LSA disponibili per i pacchetti di sicurezza in modalità LSA, vedere [Funzioni LSA chiamate da SSP/APs.](authentication-functions.md)

Per informazioni sulla registrazione di una DLL SSP/AP, vedere [Registrazione di DLL SSP/AP.](registering-ssp-ap-dlls.md)

 

 
