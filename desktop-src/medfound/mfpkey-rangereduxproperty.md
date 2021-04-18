---
description: Specifica il livello in cui il codec deve ridurre l'intervallo di colori effettivo del video.
ms.assetid: 7227957b-59c9-4dd9-ad2b-a383e888cd46
title: Proprietà MFPKEY_RANGEREDUX (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49ec326e5d21a72792aab38f08d8c8c9207ab867
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310619"
---
# <a name="mfpkey_rangeredux-property"></a>\_Proprietà RANGEREDUX di MFPKEY

Specifica il livello in cui il codec deve ridurre l'intervallo di colori effettivo del video.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMVCRangeRedux

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="default-value"></a>Valore predefinito

0

## <a name="remarks"></a>Commenti

Riduzione intervallo specifica il grado di riduzione del video da parte del codec. Riducendo l'intervallo si riducono le dimensioni dei fotogrammi video codificati, ma si riducono anche i dettagli di colore del video.

La riduzione dell'intervallo è costituita dalla riduzione durante la codifica e dall'espansione durante la decodifica. È possibile rendere i fattori di espansione diversi dai fattori di riduzione, ma ciò non è consigliabile nella maggior parte degli scenari in cui è utile il rimapping degli intervalli.

La riduzione e l'espansione dell'intervallo vengono eseguite separatamente sui canali luma e Chroma. La riduzione dell'intervallo può essere un modo efficiente per ridurre la complessità del video a bassa velocità senza sacrificare i dettagli dell'immagine. Impostando tutti e quattro i valori su 8 si riduce la quantità di dati luma e Chroma per metà, lasciando più bit da indirizzare per mantenere i dettagli dell'immagine.

Il codec può scegliere di utilizzare automaticamente la riduzione intervallo quando si codifica il video con velocità in bit molto bassa. L'impostazione di tutti e quattro i valori su 0 Disabilita completamente la riduzione dell'intervallo anche negli scenari a bassa velocità.

Riducendo l'intervallo di colori si riducono le dimensioni codificate dei fotogrammi video, ma è possibile introdurre sfocatura nei frame decodificati.

Se questa proprietà non è impostata, il codec determina se utilizzare la riduzione intervallo al momento della codifica. Questa opzione è in genere selezionata dal codec solo a velocità in bit ridotte.

Il valore di questa proprietà è costituito da una combinazione di quattro componenti, separati da zeri, formattati come 0x0M0m0N0n, in cui:

-   M è il fattore di riduzione dell'intervallo di codifica per il componente Y.
-   m è il fattore di espansione dell'intervallo di decodifica per il componente Y, in genere uguale a M.
-   N è il fattore di riduzione dell'intervallo di codifica per il componente UV.
-   n è il fattore di espansione dell'intervallo di decodifica per il componente UV (in genere uguale a N).

Ogni fattore è una cifra da 0 a 8, dove 0 non è alcuna riduzione o espansione e 8 è la riduzione o l'espansione massima.

Se si imposta il valore su 0x00000000, la riduzione dell'intervallo è completamente disabilitata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




