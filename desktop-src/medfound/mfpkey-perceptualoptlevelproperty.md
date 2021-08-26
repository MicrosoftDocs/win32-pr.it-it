---
description: Specifica se il codec deve usare l'ottimizzazione percettiva conservativa durante la codifica.
ms.assetid: f44fd932-d8f8-46c7-b17c-27e6141408ab
title: MFPKEY_PERCEPTUALOPTLEVEL proprietà (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f9eb74ae025dbddbdea7f76c2af8b15e912cf80ebd06e810a5214bf9798d1bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953851"
---
# <a name="mfpkey_perceptualoptlevel-property"></a>Proprietà MFPKEY \_ PERCEPTUALOPTLEVEL

Specifica se il codec deve usare l'ottimizzazione percettiva conservativa durante la codifica.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMVCPerceptualOptLevel

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="default-value"></a>Valore predefinito

0

## <a name="remarks"></a>Commenti

L'ottimizzazione percettiva conservativa è un processo tramite il quale il codec tenta di identificare le aree "importanti" e "non importanti" nel fotogramma video. Dopo aver identificato queste aree del frame, il codec assegna una priorità più alta alla qualità delle aree importanti, a scapito della qualità delle aree non importanti.

L'ottimizzazione percettiva evidenzia la correttezza dell'immagine all'occhio umano, invece di fare in modo che la precisione matematica sia rigorosa.

I risultati dell'ottimizzazione variano notevolmente a seconda del tipo di video da codificare. Questa funzionalità potrebbe essere particolarmente adatta per la codifica a bassa velocità in bit e a bassa risoluzione (ad esempio, lo streaming Web), ma probabilmente dovrebbe essere evitata quando si punta alla qualità video di archiviazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> </dl>

 

 




