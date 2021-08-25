---
description: Quando un'applicazione abilitata per SOAP è stata esportata da un server in modalità proxy, i client che la importano possono accedere automaticamente ai metodi dei componenti in essa contenuti, in modalità remota, come servizi Web offerti dal server in modalità CAO (Client-Activated Object). In questo modo è possibile distribuire con facilità le funzionalità di un'applicazione COM+ in una rete come servizio Web XML.
ms.assetid: 7f4783f7-4f53-4f0b-bb64-ae7903097d6c
title: Importazione di unSOAP-Enabled app
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a41a60c2b5ca69197582a684920e9e935f28631779bc632810049f1a7d03945
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858921"
---
# <a name="importing-a-soap-enabled-application"></a>Importazione di unSOAP-Enabled app

Quando un'applicazione abilitata [](exporting-a-soap-enabled-application.md) per SOAP è stata esportata da un server in modalità proxy, i client che la importano possono accedere automaticamente ai metodi dei componenti in essa contenuti, in modalità remota, come servizi Web offerti dal server in modalità CAO (Client-Activated Object). In questo modo è possibile distribuire con facilità le funzionalità di un'applicazione COM+ in una rete come servizio Web XML.

Quando i componenti di un'applicazione importata in questo modo vengono usati nel client, non vengono eseguiti nel client, ma sono invece accessibili in modalità remota usando il servizio Web XML fornito dal server da cui l'applicazione è stata esportata. Per informazioni dettagliate sull'uso dei componenti di un'applicazione importata in questo modo, vedere Accesso ai servizi [Web XML in modalità CAO.](accessing-xml-web-services-in-cao-mode.md)

## <a name="component-services-administrative-tool"></a>Strumento di amministrazione di Servizi componenti

Per importare un'applicazione abilitata per SOAP in un client, seguire questa procedura:

1.  Nell'albero della console dello strumento amministrativo Servizi componenti, in Servizi **componenti** aprire la cartella associata al computer client in cui si vuole installare l'applicazione.

2.  Fare clic con il pulsante destro del mouse sulla **cartella Applicazioni COM+ del** client e quindi scegliere **Nuovo**. Verrà **visualizzata l'Installazione guidata applicazione COM+.**

3.  **Nell'Installazione guidata applicazione COM+** fare clic su Installa applicazioni **predefinite.**

4.  Esplorare la rete per individuare o specificare il percorso di rete del file MSI nel server da cui si vuole installare l'applicazione.

## <a name="visual-basic"></a>Visual Basic

Non è valida.

## <a name="cc"></a>C/C++

Non è valida.

## <a name="remarks"></a>Commenti

I componenti COM sono identificati da un GUID, che cambia se i componenti vengono ricompilati. Se un componente COM configurato esposto come servizio Web XML viene ricompilato, le applicazioni client che lo usano verranno erre. Pertanto, quando un componente esposto come servizio Web XML viene ricompilato, i client devono reimportare le applicazioni che usano il componente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Cenni preliminari sul servizio SOAP COM+](com--soap-service-overview.md)
</dt> <dt>

[Creazione di servizi Web XML](creating-xml-web-services.md)
</dt> <dt>

[Esportazione di un'SOAP-Enabled applicazione](exporting-a-soap-enabled-application.md)
</dt> </dl>

 

 



