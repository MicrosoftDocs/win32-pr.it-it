---
description: Quando si utilizza COM+ per creare un servizio Web XML, tale servizio può essere utilizzato da qualsiasi client autorizzato, inclusi quelli che non utilizzano COM+ o anche Microsoft Windows.
ms.assetid: c40031a6-f3de-4ef4-b9aa-3f49e57da5b4
title: Esportazione di un'applicazione SOAP-Enabled
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d5c92029f431fc06964f233c5746c283821d11c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878017"
---
# <a name="exporting-a-soap-enabled-application"></a>Esportazione di un'applicazione SOAP-Enabled

Quando si utilizza COM+ per creare un servizio Web XML, tale servizio può essere utilizzato da qualsiasi client autorizzato, inclusi quelli che non utilizzano COM+ o anche Microsoft Windows. Tuttavia, l'utilizzo di un servizio Web COM+ in modalità oggetto attivato dal client da un'applicazione client COM+ è particolarmente semplice. È sufficiente esportare l'applicazione abilitata per SOAP in modalità proxy e quindi [importarla](importing-a-soap-enabled-application.md) nel client per cui si desidera accedere al servizio Web XML corrispondente.

## <a name="component-services-administrative-tool"></a>Strumento di amministrazione Servizi componenti

Per esportare un'applicazione abilitata per SOAP da un server, attenersi alla procedura seguente:

1.  Nell'albero della console dello strumento di amministrazione Servizi componenti, in **Servizi componenti**, aprire la cartella **applicazioni com+** associata al computer che si desidera gestire.

2.  Fare clic con il pulsante destro del mouse sul componente che si desidera esporre come un servizio Web XML e scegliere **Esporta**. Verrà visualizzata l' **esportazione guidata dell'applicazione com+** .

3.  Nella casella di testo **immettere il percorso completo e il nome file per il file dell'applicazione da creare**, immettere il percorso completo e il nome file per il file MSI che conterrà l'applicazione esportata oppure fare clic su **Sfoglia** per selezionare il percorso completo e il nome file utilizzando una finestra di dialogo.

4.  In **Esporta con nome** selezionare il **proxy di applicazione-installa in altri computer per abilitare l'accesso al pulsante di opzione computer** .

## <a name="visual-basic"></a>Visual Basic

Non è valida.

## <a name="cc"></a>C/C++

Non è valida.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Panoramica del servizio SOAP COM+](com--soap-service-overview.md)
</dt> <dt>

[Creazione di servizi Web XML](creating-xml-web-services.md)
</dt> <dt>

[Importazione di un'applicazione SOAP-Enabled](importing-a-soap-enabled-application.md)
</dt> </dl>

 

 



