---
title: Oggetti e proprietà
description: Le caratteristiche di un oggetto in SDO sono determinate dalle proprietà dell'oggetto e dai valori associati a tali proprietà.
ms.assetid: 9faa7759-cad5-4429-94b0-6cba145cfadb
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efed7720388e61b9d6131acafd4b9bda17694d29
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300080"
---
# <a name="objects-and-properties"></a>Oggetti e proprietà

Le caratteristiche di un oggetto in SDO sono determinate dalle proprietà dell'oggetto e dai valori associati a tali proprietà. A differenza di altri modelli a oggetti, gli oggetti SDO non dispongono di metodi. Tuttavia, gli oggetti SDO espongono interfacce COM che forniscono metodi.

Gli oggetti in SDO espongono l'interfaccia [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) che fornisce i metodi per modificare le proprietà degli oggetti. Per accedere alle proprietà dell'oggetto, ottenere un'interfaccia **ISdo** per l'oggetto e usare i metodi di interfaccia [**GetProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty) e [**PutProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-putproperty) per recuperare e impostare i valori per le proprietà. L'argomento [recupero di un SDO utente](/windows/desktop/Nps/sdo-retrieving-a-user-sdo) contiene codice di esempio che illustra come ottenere l'interfaccia **ISdo** per un oggetto utente.

Dopo avere apportato le modifiche alle proprietà di un oggetto, usare il metodo [**ISdo:: Apply**](/windows/desktop/api/sdoias/nf-sdoias-isdo-apply) per scrivere le modifiche nell'archivio permanente per l'oggetto. È possibile annullare le modifiche apportate alle proprietà di un oggetto prima di chiamare **ISdo:: Apply** chiamando il metodo [**ISdo:: Restore**](/windows/desktop/api/sdoias/nf-sdoias-isdo-restore) . Questo metodo consente di ripristinare i valori delle proprietà di un oggetto dall'archivio permanente.

Nella tabella seguente vengono illustrati i tipi di enumerazione che enumerano le proprietà di alcuni oggetti in SDO.



| Oggetto                                 | Tipo di enumerazione                                       |
|----------------------------------------|--------------------------------------------------------|
| Tutti gli oggetti SDO                        | [**IASCOMMONPROPERTIES**](/windows/desktop/api/sdoias/ne-sdoias-iascommonproperties) |
| Oggetto utente                            | [**USERPROPERTIES**](/windows/desktop/api/sdoias/ne-sdoias-userproperties)           |
| Oggetto servizio (server dei criteri di rete) | [**IASPROPERTIES**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties)             |
| Oggetto protocollo RADIUS Microsoft       | [**RADIUSPROPERTIES**](/windows/desktop/api/sdoias/ne-sdoias-radiusproperties)       |



 

> [!Note]  
> Il servizio di autenticazione Internet (IAS) è stato rinominato server dei criteri di rete (NPS) a partire da Windows Server 2008.

 

## <a name="collections"></a>Raccolte

Gli oggetti vengono spesso raggruppati in raccolte. L'API SDO fornisce funzionalità, tramite l'interfaccia di [**raccolta ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdocollection) , per enumerare gli oggetti in una raccolta e per aggiungere ed eliminare oggetti da una raccolta.

Per ottenere l'accesso a una raccolta, è necessario recuperare una proprietà di raccolta nell'oggetto che contiene la raccolta. Per ulteriori informazioni, vedere la sezione [gerarchia del modello a oggetti](/windows/desktop/Nps/sdo-object-model-hierarchy).

Il tipo di dati per tutte le proprietà che corrispondono alle raccolte è VT \_ Dispatch.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gerarchia del modello a oggetti SDO](/windows/desktop/Nps/sdo-object-model-hierarchy)
</dt> <dt>

[Attributi supportati da SDO](/windows/desktop/Nps/sdo-sdo-supported-attributes)
</dt> </dl>

 

 