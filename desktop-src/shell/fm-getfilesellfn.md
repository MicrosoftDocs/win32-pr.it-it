---
description: Inviato da un'estensione di file Manager per recuperare le informazioni relative a un file selezionato dalla finestra Active File Manager (la finestra Directory o la finestra dei risultati della ricerca). Il file selezionato può avere un nome di file lungo.
title: Messaggio FM_GETFILESELLFN (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_GETFILESELLFN
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 461fd171-d47f-41d6-953e-8e497e023ab1
ms.openlocfilehash: 847100f494772b3c59ad719d03d7bc2dbe28cc29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484045"
---
# <a name="fm_getfilesellfn-message"></a>\_Messaggio GETFILESELLFN FM

Inviato da un'estensione di file Manager per recuperare le informazioni relative a un file selezionato dalla finestra Active File Manager (la finestra Directory o la finestra dei risultati della ricerca). Il file selezionato può avere un nome di file lungo.

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

Questo messaggio deve essere utilizzato solo dalle estensioni che supportano nomi di file lunghi (ad esempio, le estensioni che supportano la rete).

Un'estensione può usare il messaggio [**FM \_ GETSELCOUNTLFN**](fm-getselcountlfn.md) per recuperare il numero di file selezionati.

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

[**\_GETFILESEL FM**](fm-getfilesel.md)
</dt> <dt>

[**\_GETSELCOUNT FM**](fm-getselcount.md)
</dt> </dl>

 

 




