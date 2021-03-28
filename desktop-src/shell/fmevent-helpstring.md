---
description: Inviato a una procedura DLL di estensione di file Manager quando il file Manager desidera una stringa della Guida per un elemento di comando del menu o della barra degli strumenti.
title: Messaggio FMEVENT_HELPSTRING (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_HELPSTRING
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 55fb5bfe-2889-40e5-9798-85f63727e31f
ms.openlocfilehash: ae3be1953d4c8bbf70f8f17fcf34fcfb1ac583f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227449"
---
# <a name="fmevent_helpstring-message"></a>\_Messaggio FMEVENT HELPSTRING

Inviato a una procedura DLL di estensione di file Manager quando il file Manager desidera una stringa della Guida per un elemento di comando del menu o della barra degli strumenti.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lpfmshs* 
</dt> <dd>

Indirizzo di una struttura [**FMS \_ HELPSTRING**](fms-helpstring.md) che comunica i dati della stringa della Guida dell'elemento di comando. La struttura **FMS \_ HELPSTRING** identifica l'elemento di comando per il quale si desidera una stringa della guida, insieme a un handle per il menu. Un'applicazione scrive quindi la stringa della guida appropriata nel membro **szHelp** della struttura **FMS \_ HELPSTRING** .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Una procedura DLL di estensione deve restituire zero se elabora questo messaggio.

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

[**\_HELPMENUITEM FMEVENT**](fmevent-helpmenuitem.md)
</dt> </dl>

 

 




