---
description: Qualsiasi applicazione COM+ può essere esposta come un servizio Web XML.
ms.assetid: 03c3d5a7-eb98-4916-b6ef-ef6aac86c574
title: Creazione di servizi Web XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b10652531e64fec38f2ac221184cb589a27b343d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304827"
---
# <a name="creating-xml-web-services"></a>Creazione di servizi Web XML

Qualsiasi applicazione COM+ può essere esposta come un servizio Web XML. I metodi nelle interfacce predefinite dei componenti configurati per le applicazioni (componenti nel catalogo COM+ Server) possono essere chiamati in remoto. È possibile utilizzare lo strumento di amministrazione Servizi componenti per creare una directory radice virtuale IIS dalla quale è possibile chiamare i metodi dei componenti utilizzando SOAP.

> [!Note]  
> Per esporre un'applicazione COM+ come un servizio Web XML, è necessario che nel computer sia installato il .NET Framework.

 

**Per esporre un'applicazione COM+ come un servizio Web XML**

1.  Nell'albero della console dello strumento di amministrazione Servizi componenti, in **Servizi componenti**, aprire la cartella **applicazioni com+** associata al computer che si desidera gestire.

2.  Fare clic con il pulsante destro del mouse sull'applicazione che si desidera esporre come un servizio Web XML e scegliere **Proprietà**.

3.  Fare clic sulla scheda **attivazione** nella finestra di dialogo Proprietà.

4.  Selezionare la casella di controllo **USA SOAP** .

5.  Nella casella di testo **SOAP vroot** immettere il nome della directory radice virtuale di IIS da cui è possibile accedere in remoto ai metodi dei componenti. Si noti che un VRoot SOAP non può essere una sottodirectory di un'altra directory VRoot SOAP.

6.  Fare clic su **OK**.

    Se si specifica la directory radice virtuale IIS come *VRoot* e il nome di dominio completo del server è *ServerName*, l'URL in cui il componente viene esposto come un servizio Web XML è https://*nomeserver* / *VRoot*/.

    La directory corrispondente nella file system è \\ Windows \\ system32 \\ com \\ SoapVRoots \\ *VRoot* \\ ; COM+ inserisce diversi file di configurazione e programmi ASP.NET. Per un servizio Web XML in condizioni di carico elevato, è consigliabile modificare i parametri archiviati nel file web.config. Per informazioni su questo file, vedere la documentazione di IIS.

    Le impostazioni di sicurezza predefinite per un'applicazione COM+ esposte come servizio Web XML variano a seconda della versione del .NET Framework installata. Se è installata la versione 1,0, i servizi Web XML non sono protetti per impostazione predefinita. tutte le chiamate vengono accettate e non viene utilizzata alcuna crittografia. Se è installata la versione 1,1 o una versione successiva, i servizi Web XML sono protetti per impostazione predefinita. i chiamanti devono essere autenticati e la crittografia è obbligatoria.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Accesso ai servizi Web XML in modalità CAO](accessing-xml-web-services-in-cao-mode.md)
</dt> <dt>

[Accesso ai servizi Web XML in modalità WKO](accessing-xml-web-services-in-wko-mode.md)
</dt> <dt>

[Panoramica del servizio SOAP COM+](com--soap-service-overview.md)
</dt> <dt>

[Protezione dei servizi Web XML](securing-xml-web-services.md)
</dt> </dl>

 

 



