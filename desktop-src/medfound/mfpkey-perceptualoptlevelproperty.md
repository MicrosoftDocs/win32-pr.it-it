---
description: Specifica se il codec deve usare l'ottimizzazione percettiva conservativa durante la codifica.
ms.assetid: f44fd932-d8f8-46c7-b17c-27e6141408ab
title: Proprietà MFPKEY_PERCEPTUALOPTLEVEL (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d86857ca9d7e4205afc0baf9c212e92606511ffc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226998"
---
# <a name="mfpkey_perceptualoptlevel-property"></a>\_Proprietà PERCEPTUALOPTLEVEL di MFPKEY

Specifica se il codec deve usare l'ottimizzazione percettiva conservativa durante la codifica.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMVCPerceptualOptLevel

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="default-value"></a>Valore predefinito

0

## <a name="remarks"></a>Commenti

L'ottimizzazione percettiva conservativa è un processo mediante il quale il codec tenta di identificare le aree "importanti" e "non importanti" nel frame del video. Dopo aver identificato queste aree del frame, il codec fornirà una priorità più elevata alla qualità delle aree importanti, a scapito della qualità delle aree non importanti.

L'ottimizzazione percettiva enfatizza l'aspetto dell'immagine come corretta per gli occhi umani, anziché insistere su una rigorosa precisione matematica.

I risultati dell'ottimizzazione variano notevolmente a seconda del tipo di video da codificare. Questa funzionalità può essere adatta per la codifica a bassa velocità di bit e bassa risoluzione (ad esempio, lo streaming web), ma dovrebbe essere evitata quando si mira alla qualità del video di archiviazione.

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

 

 




