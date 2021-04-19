---
description: Specifica se un codificatore deve essere incluso nella topologia transcodifica.
ms.assetid: 73f23aed-d1b9-4821-b1ca-0a07f02b6913
title: Attributo MF_TRANSCODE_DONOT_INSERT_ENCODER (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92d3f8fc5dabfd3e4c55c6242ba9b8f52b6f5c2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308428"
---
# <a name="mf_transcode_donot_insert_encoder-attribute"></a>\_ \_ \_ \_ Attributo encoder Insert encoder di MF transcode

Specifica se un codificatore deve essere incluso nella topologia transcodifica.

La funzione [**MFCreateTranscodeTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) controlla questo attributo durante la compilazione della topologia. Se questo attributo non è impostato, nella topologia transcodifica viene inserito un codificatore.

## <a name="data-type"></a>Tipo di dati

**UINT32**



| Valore                                                                        | Significato                                                                                                           |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Viene inserito un codificatore nella topologia transcodifica.<br/>                                                      |
| <dl> <dt>1</dt> </dl> | Un codificatore non è incluso nella topologia transcodifica. Il nodo di origine è connesso al nodo di output.<br/> |



 

## <a name="remarks"></a>Commenti

La costante GUID per questo attributo viene esportata da mfuuid. lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                         |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                            |
| Intestazione<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi di Media Foundation](media-foundation-attributes.md)
</dt> </dl>

 

 




