---
description: Inviato da un'estensione di file Manager per recuperare le informazioni relative a un file selezionato dalla finestra Active File Manager (la finestra Directory o la finestra dei risultati della ricerca).
title: Messaggio FM_GETFILESEL (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_GETFILESEL
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: c2b4aac6-165b-4eba-b012-ee7a20481cd3
ms.openlocfilehash: ec7d221e0c352c4b9284ae5fe2d6f80e50da85ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881590"
---
# <a name="fm_getfilesel-message"></a>\_Messaggio GETFILESEL FM

Inviato da un'estensione di file Manager per recuperare le informazioni relative a un file selezionato dalla finestra Active File Manager (la finestra Directory o la finestra dei risultati della ricerca).

## <a name="parameters"></a>Parametri

<dl> <dt>

*index* 
</dt> <dd>

Indice in base zero del file selezionato da recuperare.

</dd> <dt>

*lpfmsgfs* 
</dt> <dd>

Indirizzo di una struttura [**FMS \_ GETFILESEL**](fms-getfilesel.md) che riceve informazioni sulla selezione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'indice in base zero del file selezionato recuperato.

## <a name="remarks"></a>Commenti

Un'estensione può usare il messaggio [**FM \_ GETSELCOUNT**](fm-getselcount.md) per recuperare il numero di file selezionati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Wfext. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> <dt>

[**\_GETFILESELLFN FM**](fm-getfilesellfn.md)
</dt> <dt>

[**\_GETSELCOUNTLFN FM**](fm-getselcountlfn.md)
</dt> </dl>

 

 




