---
description: Inviato a una procedura DLL di estensione di File Manager quando File Manager vuole una stringa della Guida per un menu o una voce di comando della barra degli strumenti.
title: FMEVENT_HELPSTRING messaggio (Wfext.h)
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
ms.openlocfilehash: 06e3c13841c6b4dc85c2a1dcbea7dce18a15ab054ffb2953fa2e3ba2999d5863
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119094156"
---
# <a name="fmevent_helpstring-message"></a>Messaggio \_ HELPSTRING FMEVENT

Inviato a una procedura DLL di estensione di File Manager quando File Manager vuole una stringa della Guida per un menu o una voce di comando della barra degli strumenti.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lpfmshs* 
</dt> <dd>

Indirizzo di una struttura [**\_ HELPSTRING FMS**](fms-helpstring.md) che comunica i dati della stringa della Guida dell'elemento del comando. La **struttura FMS \_ HELPSTRING** identifica l'elemento di comando per il quale è ricercata una stringa della Guida, insieme a un handle al relativo menu. Un'applicazione scrive quindi la stringa della Guida appropriata nel membro **szHelp** della struttura **\_ HELPSTRING FMS.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Una routine DLL di estensione deve restituire zero se elabora questo messaggio.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Wfext.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> <dt>

[**FMEVENT \_ HELPMENUITEM**](fmevent-helpmenuitem.md)
</dt> </dl>

 

 




