---
title: Costanti di enumerazione (WSManDisp.h)
description: L'enumerazione contiene costanti, come elencato nell'elenco seguente, usate nel parametro flags dalle chiamate a Session.Enumerate e IWSManSession Enumerate.
ms.assetid: c0f2763b-a549-43d5-84a6-8cebf33a1ea2
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- WSManFlagReturnObject
- WSManFlagNonXmlText
- EnumerationFlagReturnEPR
- WSManFlagReturnObjectAndEPR
- WSManFlagHierarchyDeep
- WSManFlagHierarchyShallow
- WSManFlagHierarchyDeepBasePropsOnly
api_location:
- WSManDisp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9c8182352d2ebf3763a38f74dd6f100dc836e88cfa10212ffaa971048ebd1aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118113263"
---
# <a name="enumeration-constants"></a>Costanti di enumerazione

**\_ \_ L'enumerazione WSManEnumFlags** contiene costanti, come elencato nell'elenco seguente, usate nel parametro *flags* dalle chiamate a [**Session.Enumerate**](session-enumerate.md) e [**IWSManSession::Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate).

Tenere presente che **WSManFlagReturnObject** e **WSManFlagHierarchyDeep** sono l'impostazione predefinita se il *parametro flags* non è specificato.

<dl> <dt>

<span id="WSManFlagReturnObject"></span><span id="wsmanflagreturnobject"></span><span id="WSMANFLAGRETURNOBJECT"></span>**Oggetto WSManFlagReturnObject**
</dt> <dd> <dl> <dt>

0 (0x0)
</dt> <dt>



I batch contengono le istanze XML richieste. Si tratta del valore predefinito per il parametro flag.

Il metodo di scripting associato [**è WSMan.EnumerationFlagReturnObject**](wsman-enumerationflagreturnobject.md) e il metodo C++ [**è IWSManEx.EnumerationFlagReturnObject**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnobject).


</dt> </dl> </dd> <dt>

<span id="WSManFlagNonXmlText"></span><span id="wsmanflagnonxmltext"></span><span id="WSMANFLAGNONXMLTEXT"></span>**WSManFlagNonXmlText**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



Questo flag controlla il modo in *cui il* parametro di filtro nella chiamata [**a Session.Enumerate**](session-enumerate.md) viene interpretato da WinRM.

Il formato del filtro può essere un frammento XML o una stringa di testo normale. Il formato è determinato dal [*dialetto*](windows-remote-management-glossary.md) di filtro usato nella chiamata a [**Session.Enumerate**](session-enumerate.md) o [**IWSManSession::Enumerate,**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate)specifico per l'operazione eseguita. [](windows-remote-management-glossary.md)

Se il *parametro dialect* non è specificato, WinRM tenta di determinare il dialetto in base al primo carattere del filtro. Se il primo carattere è <, ma il filtro non è effettivamente un frammento XML, è necessario impostare questo flag. Ad esempio, per un filtro nel formato seguente è necessario impostare **WSManFlagNonXmlText** in modo che il filtro venga interpretato correttamente:

`<25 && > 1`

Se il filtro è un frammento XML, questo flag non è necessario perché il frammento inizia con <, che WinRM interpreta correttamente come XML. Ad esempio,

`<filter>select * from aDataStructure</filter>`

Se il filtro è in testo normale che non inizia con <, questo flag non è obbligatorio. Ad esempio,

`select * from aDataStructure`

Il metodo di scripting associato [**è WSMan.EnumerationFlagNonXmlText**](wsman-enumerationflagnonxmltext.md) e il metodo C++ [**è IWSManEx.EnumerationFlagNonXmlText**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagnonxmltext).


</dt> </dl> </dd> <dt>

<span id="EnumerationFlagReturnEPR"></span><span id="enumerationflagreturnepr"></span><span id="ENUMERATIONFLAGRETURNEPR"></span>**EnumerationFlagReturnEPR**
</dt> <dd> <dl> <dt>

2 (0x2)
</dt> <dt>



I batch contengono riferimenti endpoint (EPR) per le istanze XML corrispondenti, ma non le istanze effettive.

Il metodo di scripting associato [**è WSMan.EnumerationFlagReturnEPR**](wsman-enumerationflagreturnepr.md) e il metodo C++ [**è IWSManEx.EnumerationFlagReturnEPR**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnepr).


</dt> </dl> </dd> <dt>

<span id="WSManFlagReturnObjectAndEPR"></span><span id="wsmanflagreturnobjectandepr"></span><span id="WSMANFLAGRETURNOBJECTANDEPR"></span>**WSManFlagReturnObjectAndEPR**
</dt> <dd> <dl> <dt>

4 (0x4)
</dt> <dt>



I batch contengono sia le istanze XML richieste che le EPR corrispondenti contenute in un [*elemento wsman:Items.*](windows-remote-management-glossary.md)

Il metodo di scripting associato è [**WSMan.EnumerationFlagReturnObjectAndEPR**](wsman-enumerationflagreturnobjectandepr.md) e il metodo C++ [**è IWSManEx.EnumerationFlagReturnObjectAndEPR**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnobjectandepr).


</dt> </dl> </dd> <dt>

<span id="WSManFlagHierarchyDeep"></span><span id="wsmanflaghierarchydeep"></span><span id="WSMANFLAGHIERARCHYDEEP"></span>**WSManFlagHierarchyDeep**
</dt> <dd> <dl> <dt>

0 (0x0)
</dt> <dt>



Le istanze delle classi derivate sono incluse e sono rappresentate in base ai relativi schemi effettivi.

Il metodo di scripting associato è [**WSMan.EnumerationFlagHierarchyDeep**](wsman-enumerationflaghierarchydeep.md) e il metodo C++ [**è IWSManEx.EnumerationFlagHierarchyDeep**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchydeep).


</dt> </dl> </dd> <dt>

<span id="WSManFlagHierarchyShallow"></span><span id="wsmanflaghierarchyshallow"></span><span id="WSMANFLAGHIERARCHYSHALLOW"></span>**WSManFlagHierarchyShallow**
</dt> <dd> <dl> <dt>

32 (0x20)
</dt> <dt>



Le istanze delle classi derivate sono escluse. Vengono visualizzate solo le istanze del tipo richiesto.

Il metodo di scripting associato [**è WSMan.EnumerationFlagHierarchyShallow**](wsman-enumerationflaghierarchyshallow.md) e il metodo C++ [**è IWSManEx.EnumerationFlagHierarchyShallow.**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchyshallow)


</dt> </dl> </dd> <dt>

<span id="WSManFlagHierarchyDeepBasePropsOnly"></span><span id="wsmanflaghierarchydeepbasepropsonly"></span><span id="WSMANFLAGHIERARCHYDEEPBASEPROPSONLY"></span>**WSManFlagHierarchyDeepBasePropsOnly**
</dt> <dd> <dl> <dt>

64 (0x40)
</dt> <dt>



Le istanze delle classi derivate sono incluse e sono rappresentate in base allo schema della classe di base. Le proprietà definite nella classe derivata non vengono visualizzate.

Il metodo di scripting associato è [**WSMan.EnumerationFlagHierarchyDeepBasePropsOnly**](wsman-enumerationflaghierarchydeepbasepropsonly.md) e il metodo C++ [**è IWSManEx.EnumerationFlagHierarchyDeepBasePropsOnly.**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchydeepbasepropsonly)


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                 |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                           |
| Intestazione<br/>                   | <dl> <dt>WSManDisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>WSManDisp.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti ed enumerazioni WinRM](winrm-constants-and-enumerations.md)
</dt> <dt>

[Enumerazione o elenco di tutte le istanze di una risorsa](enumerating-or-listing-all-instances-of-a-resource.md)
</dt> <dt>

[Esecuzione di query per istanze specifiche di una risorsa](querying-for-specific-instances-of-a-resource.md)
</dt> </dl>

 

 





