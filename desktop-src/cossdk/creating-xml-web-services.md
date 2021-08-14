---
description: Qualsiasi applicazione COM+ può essere esposta come servizio Web XML.
ms.assetid: 03c3d5a7-eb98-4916-b6ef-ef6aac86c574
title: Creazione di servizi Web XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12dbc5ee08d9300d52b538648ba520b16a60a9e3769242c252eaa40d518a3ea1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118307338"
---
# <a name="creating-xml-web-services"></a>Creazione di servizi Web XML

Qualsiasi applicazione COM+ può essere esposta come servizio Web XML. I metodi nelle interfacce predefinite dei componenti configurati delle applicazioni (componenti nel catalogo COM+ dei server) possono quindi essere chiamati in modalità remota. È possibile usare lo strumento amministrativo Servizi componenti per creare una directory radice virtuale IIS da cui è possibile chiamare i metodi del componente tramite SOAP.

> [!Note]  
> Il .NET Framework deve essere installato nel computer per esporre un'applicazione COM+ come servizio Web XML.

 

**Per esporre un'applicazione COM+ come servizio Web XML**

1.  Nell'albero della console dello strumento amministrativo Servizi componenti, in Servizi **componenti** aprire la **cartella Applicazioni COM+** associata al computer da gestire.

2.  Fare clic con il pulsante destro del mouse sull'applicazione che si vuole esporre come servizio Web XML e scegliere **Proprietà**.

3.  Fare clic **sulla scheda Attivazione** nella finestra di dialogo delle proprietà.

4.  Selezionare la **casella di controllo Usa SOAP.**

5.  Nella casella **di testo SOAP VRoot** immettere il nome della directory radice virtuale IIS da cui è possibile accedere in modalità remota ai metodi dei componenti. Si noti che una VRoot SOAP non può essere una sottodirectory di un'altra directory VRoot SOAP.

6.  Fare clic su **OK**.

    Se si specifica la directory radice virtuale IIS come *vroot* e il nome di dominio completo dei server è *servername*, l'URL in cui il componente viene esposto come servizio Web XML è https://*nomeserver* / *vroot*/.

    La directory corrispondente nel file system è \\ windows \\ system32 \\ com \\ SoapVRoots \\ *vroot* \\ ; COM+ inserisce diversi file di configurazione e ASP.NET programmi. Per un servizio Web XML con carico elevato, è possibile modificare i parametri archiviati nel file web.config. Per informazioni su questo file, vedere la documentazione di IIS.

    Le impostazioni di sicurezza predefinite per un'applicazione COM+ esposte come servizio Web XML variano a seconda della versione del .NET Framework installata. Se è installata la versione 1.0, i servizi Web XML non sono sicuri per impostazione predefinita. tutte le chiamate vengono accettate e non viene usata alcuna crittografia. Se è installata la versione 1.1 o successiva, i servizi Web XML sono protetti per impostazione predefinita. I chiamanti devono essere autenticati ed è necessaria la crittografia.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Accesso ai servizi Web XML in modalità CAO](accessing-xml-web-services-in-cao-mode.md)
</dt> <dt>

[Accesso ai servizi Web XML in modalità WKO](accessing-xml-web-services-in-wko-mode.md)
</dt> <dt>

[Cenni preliminari sul servizio SOAP COM+](com--soap-service-overview.md)
</dt> <dt>

[Protezione dei servizi Web XML](securing-xml-web-services.md)
</dt> </dl>

 

 



