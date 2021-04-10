---
title: Servizio trasferimento intelligente in background
description: Servizio trasferimento intelligente in background (BITS) consente di trasferire file (download o caricamenti) tra un client e un server e offre informazioni sullo stato correlate ai trasferimenti.
ms.assetid: ce91f87c-8273-4a1c-99e0-ef55e2a50334
keywords:
- Servizio trasferimento intelligente in background
- Servizio trasferimento intelligente in background, pagina iniziale
- BITS (vedere Servizio trasferimento intelligente in background)
- download dei bit di file
- BIT di trasferimento file in background
- caricamento di bit di file
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: a531821665490735b391ab2714f5b37146c6bc1e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963330"
---
# <a name="background-intelligent-transfer-service"></a>Servizio trasferimento intelligente in background

## <a name="purpose"></a>Scopo

Servizio trasferimento intelligente in background (BITS) viene usato dai programmatori e dagli amministratori di sistema per scaricare file o caricare file in server Web HTTP e condivisioni file SMB. BITS prenderà in considerazione il costo del trasferimento e l'utilizzo della rete, in modo che il lavoro in primo piano dell'utente abbia il minor impatto possibile. BITS gestisce anche il interuptions di rete, la sospensione e la ripresa automatica di trasferimenti, anche dopo un riavvio. BITS include i cmdlet di PowerShell per la creazione e la gestione dei trasferimenti, nonché l'utilità della riga di comando BitsAdmin.

> [!Note]  
> BITS può essere usato da Windows per scaricare gli aggiornamenti nel sistema locale. Se si è un utente finale che cerca modi per risolvere i problemi di installazione BITS, vedere [risolvere i problemi di Windows Update](https://support.microsoft.com/help/10164/fix-windows-update-errors). 
 

## <a name="where-applicable"></a>Se applicabile

Usare BITS per le applicazioni che devono:

-   Scaricare o caricare file in un server Web HTTP o REST o in un file server SMB.
-   Riavvia automaticamente i trasferimenti di file dopo la disconnessione della rete e il riavvio del computer.
-   Mantenere la velocità di risposta delle altre applicazioni di rete.
-   Tenere in considerazione il costo di rete, ad esempio le reti mobili
-   Usare facoltativamente [BranchCache](/windows-server/networking/branchcache/branchcache) per ottimizzare il traffico di Wide Area Network (WAN)

## <a name="developer-audience"></a>Sviluppatori

BITS è un'interfaccia COM progettata per sviluppatori C e C++ che può essere usata anche dagli sviluppatori .NET. Gli sviluppatori UWP devono usare l'API [Windows. Networking. BackgroundTransfer](/uwp/api/Windows.Networking.BackgroundTransfer) e non l'API BITS.

## <a name="bits-versions"></a>Versioni BITS

Per informazioni complete sulla cronologia delle versioni e informazioni sul sistema operativo precedente [, vedere Novità](what-s-new.md).


## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                           | Descrizione                                                                                                                                                                     |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Informazioni su BITS](about-bits.md)<br/>                         | Informazioni generali sui bit.<br/>                                                                                                                                      |
| [Uso di BITS](using-bits.md)<br/>                         | Guida procedurale per lo sviluppo di client BITS che trasferiscono file tra un client e un server.<br/>                                                                        |
| [Riferimenti BITS](bits-reference.md)<br/>                 | Informazioni di riferimento per le interfacce di programmazione BITS. Contiene inoltre informazioni su esempi, strumenti, impostazioni server per i processi di caricamento e il protocollo di caricamento.<br/> |
| [Procedure consigliate](best-practices-when-using-bits.md)<br/> | Informazioni da considerare quando si progetta un'applicazione che utilizza BITS.<br/>                                                                                                |



 

## <a name="additional-resources"></a>Risorse aggiuntive

Di seguito sono riportate altre risorse.


|             |                                                                                                                                                 |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| DLL di riferimento .NET   | Per informazioni sull'uso di BITS da .NET con le DLL di riferimento, vedere la pagina relativa alla [chiamata a BITS da .NET tramite dll di riferimento](/windows/desktop/Bits/bits-dot-net)      |
| Wrapper .NET   | Per gli altri wrapper .NET per BITS, è possibile cercare i progetti contrassegnati con il tag BITS in [NuGet](https://www.nuget.org/packages?q=Tags%3A%22BITS%22) .        |



 

 

