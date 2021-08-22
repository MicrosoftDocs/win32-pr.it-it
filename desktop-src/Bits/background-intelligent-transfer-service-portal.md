---
title: Servizio trasferimento intelligente in background
description: Servizio trasferimento intelligente in background (BITS) consente di trasferire file (download o caricamenti) tra un client e un server e offre informazioni sullo stato correlate ai trasferimenti.
ms.assetid: ce91f87c-8273-4a1c-99e0-ef55e2a50334
keywords:
- Servizio trasferimento intelligente in background
- Servizio trasferimento intelligente in background, pagina iniziale
- BITS (vedere Servizio trasferimento intelligente in background)
- download di file BITS
- BITS per il trasferimento di file in background
- caricamento di file BITS
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: 66bc9af5231454ef63d8c74f9e500baaeb7c8cec9dbdd694943a3809da4a391d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588731"
---
# <a name="background-intelligent-transfer-service"></a>Servizio trasferimento intelligente in background

## <a name="purpose"></a>Scopo

Servizio trasferimento intelligente in background (BITS) viene usato dai programmatori e dagli amministratori di sistema per scaricare o caricare file in server Web HTTP e condivisioni file SMB. BITS prenderà in considerazione il costo del trasferimento, nonché l'utilizzo della rete, in modo che il lavoro in primo piano dell'utente abbia il minimo impatto possibile. BITS gestisce anche le interuption di rete, la sospensione e la ripresa automatica dei trasferimenti, anche dopo un riavvio. BITS include i cmdlet di PowerShell per la creazione e la gestione dei trasferimenti, nonché l'utilità della riga di comando BitsAdmin.

> [!Note]  
> BITS può essere usato da Windows scaricare gli aggiornamenti nel sistema locale. Se si è un utente finale alla ricerca di modi per risolvere i problemi di installazione di BITS, vedere Risolvere Windows [problemi di aggiornamento](https://support.microsoft.com/help/10164/fix-windows-update-errors). 
 

## <a name="where-applicable"></a>Se applicabile

Usare BITS per le applicazioni che devono:

-   Scaricare o caricare file in un server Web HTTP o REST o in un file server.
-   Riprendere automaticamente i trasferimenti di file dopo la disconnessione della rete e il riavvio del computer.
-   Mantenere la velocità di risposta di altre applicazioni di rete.
-   Tenere presente il costo della rete per le reti mobili, ad esempio
-   Facoltativamente, usare [BranchCache per](/windows-server/networking/branchcache/branchcache) ottimizzare il traffico wan (Wide Area Network)

## <a name="developer-audience"></a>Sviluppatori

BITS è un'interfaccia COM progettata per gli sviluppatori C e C++ che può essere usata anche dagli sviluppatori .NET. Gli sviluppatori UWP devono usare il [Windows. API Networking.BackgroundTransfer](/uwp/api/Windows.Networking.BackgroundTransfer) e non API BITS.

## <a name="bits-versions"></a>Versioni bits

Per informazioni complete sulla cronologia delle versioni e sul sistema operativo precedente, vedere [Novità di](what-s-new.md).


## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                           | Descrizione                                                                                                                                                                     |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Informazioni su BITS](about-bits.md)<br/>                         | Informazioni generali su BITS.<br/>                                                                                                                                      |
| [Uso di BITS](using-bits.md)<br/>                         | Guida procedurale per lo sviluppo di client BITS che trasferiscono file tra un client e un server.<br/>                                                                        |
| [Riferimenti BITS](bits-reference.md)<br/>                 | Informazioni di riferimento per le interfacce di programmazione BITS. Contiene anche informazioni sugli esempi, gli strumenti, le impostazioni del server per i processi di caricamento e il protocollo di caricamento.<br/> |
| [Procedure consigliate](best-practices-when-using-bits.md)<br/> | Informazioni da considerare durante la progettazione di un'applicazione che usa BITS.<br/>                                                                                                |



 

## <a name="additional-resources"></a>Risorse aggiuntive

Di seguito sono riportate altre risorse.


|    Risorsa         |    Descrizione                                                                                                                                     |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| DLL di riferimento .NET   | Per informazioni sull'uso di BITS da .NET tramite DLL di riferimento, vedere Chiamata a BITS da [.NET tramite DLL di riferimento](/windows/desktop/Bits/bits-dot-net)      |
| Wrapper .NET   | Per altri wrapper .NET per BITS, è possibile cercare i progetti [contrassegnati](https://www.nuget.org/packages?q=Tags%3A%22BITS%22) con il tag BITS.        |



 

 

