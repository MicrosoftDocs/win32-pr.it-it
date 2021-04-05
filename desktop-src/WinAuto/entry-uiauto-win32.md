---
title: Automazione interfaccia utente
description: Automazione interfaccia utente Microsoft è un Framework di accessibilità che consente alle applicazioni Windows di fornire e utilizzare informazioni programmatiche sulle interfacce utente.
ms.assetid: 700ca38d-ff40-472b-a95a-11fa94c3bc1d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8006c79299cc1f736dc43555968443f634d4a51
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872769"
---
# <a name="ui-automation"></a>Automazione interfaccia utente

Automazione interfaccia utente Microsoft è un Framework di accessibilità che consente alle applicazioni Windows di fornire e utilizzare informazioni programmatiche sulle interfacce utente. Consente l'accesso a livello di codice alla maggior parte degli elementi dell'interfaccia utente sul desktop. Consente ai prodotti di Assistive Technology, quali utilità per la lettura dello schermo, di fornire informazioni sull'interfaccia utente agli utenti finali e di modificare l'interfaccia utente per mezzo di input standard. Automazione interfaccia utente consente inoltre l'interazione degli script di test automatizzati con l'interfaccia utente.

-   [Ove applicabile](#where-applicable)
-   [Destinatari degli sviluppatori](#developer-audience)
-   [Requisiti della fase di esecuzione](#run-time-requirements)
-   [Supporto per sistemi operativi di livello inferiore](#support-for-down-level-operating-systems)

## <a name="where-applicable"></a>Ambito di applicazione

Utilizzando l'automazione interfaccia utente e le seguenti procedure di progettazione accessibili, gli sviluppatori possono rendere le applicazioni in esecuzione in Windows più accessibili a molti utenti con problemi di visione, udito o movimento. Inoltre, l'automazione dell'interfaccia utente è progettata appositamente per fornire funzionalità affidabili per gli scenari di test automatizzati.

## <a name="developer-audience"></a>Sviluppatori

Automazione interfaccia utente è progettata per gli sviluppatori C/C++ esperti. In generale, gli sviluppatori necessitano di un livello moderato di informazioni sugli oggetti e le interfacce di Component Object Model (COM), Unicode e la programmazione dell'API Windows.

Per informazioni sull'automazione dell'interfaccia utente per il codice gestito, vedere l'articolo relativo all' [accessibilità](/dotnet/framework/ui-automation/) nella sezione della Guida per sviluppatori .NET Framework di MSDN.

## <a name="run-time-requirements"></a>Requisiti di runtime

Automazione interfaccia utente è supportata nei sistemi operativi seguenti: Windows XP, Windows Server 2003, Windows Server 2003 R2, Windows Vista, Windows 7, Windows 10, Windows Server 2008, Windows Server 2008 R2, Windows Server 2012, Windows Server 2012 R2, Windows Server 2016 e Windows Server 2019.

> [!Note]  
> Windows XP e Windows Server 2003 richiedono anche Microsoft .NET Framework 3,0.

 

## <a name="support-for-down-level-operating-systems"></a>Supporto per sistemi operativi di livello inferiore

L'aggiornamento della piattaforma per Windows Vista è costituito da un set di librerie di runtime che consente agli sviluppatori di utilizzare le applicazioni sia per i sistemi operativi Windows 7 che per quelli di livello inferiore. L'aggiornamento della piattaforma per Windows Server 2008 è costituito da un set di librerie di runtime che consente agli sviluppatori di utilizzare le applicazioni in Windows Server 2008 R2 e versioni precedenti di Windows Server. L'aggiornamento della piattaforma per Windows Vista e l'aggiornamento della piattaforma per Windows Server 2008 saranno disponibili per tutti i clienti di Windows Vista e Windows Server 2008 tramite Windows Update. Le applicazioni di terze parti che richiedono l'aggiornamento della piattaforma per Windows Vista o l'aggiornamento della piattaforma per Windows Server 2008 possono avere Windows Update rilevare se è installato; in caso contrario, Windows Update lo scaricherà e installerà in background.

L'aggiornamento della piattaforma per Windows Vista e l'aggiornamento della piattaforma per Windows Server 2008 supportano entrambi l'intero set di funzionalità dell'API di automazione Windows 3,0 nei sistemi operativi seguenti.

-   Windows XP (Inglese) <dl> Windows XP Home SP3 x86  
    Windows XP Professional SP3 x86  
    </dl>
-   Windows Server 2003 (English) <dl> Windows Server 2003 SP2 (x86 e x64)  
    </dl>
-   Windows Vista (Inglese) <dl> Starter SP2 (x86 e x64)  
    Home Premium SP2 (x86 e x64)  
    Business SP2 (x86 e x64)  
    Enterprise SP2 (x86 e x64)  
    Ultimate SP2 (x86 e x64)  
    </dl>
-   Windows Server 2008 (Inglese) <dl> Windows Server 2008 SP2 (x86 e x64)  
    </dl>

Per ulteriori informazioni su entrambi gli aggiornamenti, vedere [aggiornamento della piattaforma per Windows Vista](../win7ip/platform-update-for-windows-vista-portal.md).

## <a name="in-this-section"></a>Contenuto della sezione

-   [Nozioni fondamentali sull'automazione interfaccia utente](entry-uiautocore-overview.md)
-   [Guida per programmatori del provider di automazione interfaccia utente](uiauto-providerportal.md)
-   [Guida per programmatori client di automazione interfaccia utente](uiauto-clientportal.md)
-   [Riferimento](entry-uiautocore-ref.md)
-   [Esempi](samples-entry.md)
-   [Appendici](appendix-entry.md)

 

 