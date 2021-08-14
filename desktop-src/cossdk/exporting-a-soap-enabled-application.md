---
description: Quando si usa COM+ per creare un servizio Web XML, tale servizio può essere utilizzato da qualsiasi client autorizzato, inclusi quelli che non usano COM+ o anche Microsoft Windows.
ms.assetid: c40031a6-f3de-4ef4-b9aa-3f49e57da5b4
title: Esportazione di un'SOAP-Enabled applicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce79bbc5dca59feb23ba9e976575b3b33570ecd27cf1e6a68560b02e073f48bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118307288"
---
# <a name="exporting-a-soap-enabled-application"></a>Esportazione di un'SOAP-Enabled applicazione

Quando si usa COM+ per creare un servizio Web XML, tale servizio può essere utilizzato da qualsiasi client autorizzato, inclusi quelli che non usano COM+ o anche Microsoft Windows. Tuttavia, l'uso di un servizio Web COM+ in modalità oggetto attivato dal client (CAO) da un'applicazione client COM+ è particolarmente semplice. È sufficiente esportare l'applicazione abilitata [](importing-a-soap-enabled-application.md) per SOAP in modalità proxy e quindi importarla nel client per il quale si desidera accedere al servizio Web XML corrispondente.

## <a name="component-services-administrative-tool"></a>Strumento di amministrazione Servizi componenti

Per esportare un'applicazione abilitata per SOAP da un server, seguire questa procedura:

1.  Nell'albero della console dello strumento di amministrazione Servizi componenti, in Servizi componenti **aprire** la cartella **Applicazioni COM+** associata al computer da gestire.

2.  Fare clic con il pulsante destro del mouse sul componente che si vuole esporre come servizio Web XML e scegliere **Esporta.** Verrà **visualizzata l'Esportazione guidata applicazioni COM+.**

3.  Nella casella di testo immettere il percorso completo e il nome del **file** dell'applicazione da creare, immettere il percorso  completo e il nome del file MSI che conterrà l'applicazione esportata oppure fare clic su Sfoglia per selezionare il percorso completo e il nome file usando una finestra di dialogo.

4.  In **Esporta come** selezionare il pulsante di opzione Application Proxy - Installa in altri computer per abilitare **l'accesso a questo** computer.

## <a name="visual-basic"></a>Visual Basic

Non è valida.

## <a name="cc"></a>C/C++

Non è valida.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Cenni preliminari sul servizio SOAP COM+](com--soap-service-overview.md)
</dt> <dt>

[Creazione di servizi Web XML](creating-xml-web-services.md)
</dt> <dt>

[Importazione di un'SOAP-Enabled applicazione](importing-a-soap-enabled-application.md)
</dt> </dl>

 

 



