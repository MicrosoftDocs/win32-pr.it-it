---
description: Quando un'applicazione abilitata per SOAP è stata esportata da un server in modalità proxy, i client che lo importano possono accedere automaticamente ai metodi dei componenti che contiene, in modalità remota, come servizi Web offerti dal server in modalità oggetto attivato dal client. In questo modo è possibile distribuire con facilità la funzionalità di un'applicazione COM+ in una rete come un servizio Web XML.
ms.assetid: 7f4783f7-4f53-4f0b-bb64-ae7903097d6c
title: Importazione di un'applicazione SOAP-Enabled
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d9faca91a726caea765d4b2ca227ddba0ff3a2f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524201"
---
# <a name="importing-a-soap-enabled-application"></a>Importazione di un'applicazione SOAP-Enabled

Quando un'applicazione abilitata per SOAP è stata [esportata](exporting-a-soap-enabled-application.md) da un server in modalità proxy, i client che lo importano possono accedere automaticamente ai metodi dei componenti che contiene, in modalità remota, come servizi Web offerti dal server in modalità oggetto attivato dal client. In questo modo è possibile distribuire con facilità la funzionalità di un'applicazione COM+ in una rete come un servizio Web XML.

Quando i componenti di un'applicazione importati in questo modo vengono utilizzati nel client, non vengono eseguiti sul client ma vengono invece accessibili in modalità remota utilizzando il servizio Web XML fornito dal server da cui è stata esportata l'applicazione. Per informazioni dettagliate sull'uso dei componenti di un'applicazione importata in questo modo, vedere [accesso ai servizi Web XML in modalità Cao](accessing-xml-web-services-in-cao-mode.md).

## <a name="component-services-administrative-tool"></a>Strumento di amministrazione Servizi componenti

Per importare un'applicazione abilitata per SOAP in un client, attenersi alla procedura seguente:

1.  Nell'albero della console dello strumento di amministrazione Servizi componenti, in **Servizi componenti**, aprire la cartella associata al computer client in cui si desidera installare l'applicazione.

2.  Fare clic con il pulsante destro del mouse sulla cartella **applicazioni com+** del client, quindi scegliere **nuovo**. Verrà visualizzata la **procedura guidata di installazione dell'applicazione com+** .

3.  Nella **procedura guidata di installazione dell'applicazione com+**, fare clic su **Installa applicazione**/e predefinita.

4.  Esplorare la rete per individuare o specificare il percorso di rete del file MSI nel server da cui si desidera installare l'applicazione.

## <a name="visual-basic"></a>Visual Basic

Non è valida.

## <a name="cc"></a>C/C++

Non è valida.

## <a name="remarks"></a>Commenti

I componenti COM sono identificati da un GUID, che cambia se i componenti vengono ricompilati. Se un componente COM configurato esposto come un servizio Web XML viene ricompilato, le applicazioni client che lo utilizzano si interromperanno. Pertanto, quando un componente esposto come un servizio Web XML viene ricompilato, i client devono importare nuovamente le applicazioni che utilizzano il componente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Panoramica del servizio SOAP COM+](com--soap-service-overview.md)
</dt> <dt>

[Creazione di servizi Web XML](creating-xml-web-services.md)
</dt> <dt>

[Esportazione di un'applicazione SOAP-Enabled](exporting-a-soap-enabled-application.md)
</dt> </dl>

 

 



