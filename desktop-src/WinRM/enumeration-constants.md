---
title: Costanti di enumerazione (WSManDisp. h)
description: L'enumerazione contiene costanti, elencate nell'elenco seguente, utilizzate nel parametro flags dalle chiamate a Session. enumerate e IWSManSession.
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
ms.openlocfilehash: e422f688fea992ee2d9b1d0d25af00a1d24ad798
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400428"
---
# <a name="enumeration-constants"></a>Costanti di enumerazione

L'enumerazione **\_ \_ WSManEnumFlags** contiene costanti, elencate nell'elenco seguente, utilizzate nel parametro *Flags* dalle chiamate a [**Session. enumerate**](session-enumerate.md) e [**IWSManSession:: enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate).

Tenere presente che **WSManFlagReturnObject** e **WSManFlagHierarchyDeep** sono i valori predefiniti se il parametro *Flags* non è specificato.

<dl> <dt>

<span id="WSManFlagReturnObject"></span><span id="wsmanflagreturnobject"></span><span id="WSMANFLAGRETURNOBJECT"></span>**WSManFlagReturnObject**
</dt> <dd> <dl> <dt>

0 (0x0)
</dt> <dt>



I batch contengono le istanze XML richieste. Si tratta del valore predefinito per il parametro del flag.

Il metodo di scripting associato è [**WSMan. EnumerationFlagReturnObject**](wsman-enumerationflagreturnobject.md) e il metodo C++ è [**IWSManEx. EnumerationFlagReturnObject**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnobject).


</dt> </dl> </dd> <dt>

<span id="WSManFlagNonXmlText"></span><span id="wsmanflagnonxmltext"></span><span id="WSMANFLAGNONXMLTEXT"></span>**WSManFlagNonXmlText**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



Questo flag controlla il modo in cui il parametro *Filter* nella chiamata a [**Session. enumerate**](session-enumerate.md) viene interpretato da WinRM.

Il formato del filtro può essere un frammento XML o una stringa di testo normale. Il formato è determinato dal [*dialetto del filtro*](windows-remote-management-glossary.md) [*utilizzato nella*](windows-remote-management-glossary.md) chiamata a [**Session. enumerate**](session-enumerate.md) o [**IWSManSession:: enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate), che è specifico dell'operazione eseguita.

Se il parametro *dialect* non è specificato, WinRM tenta di determinare il dialetto in base al primo carattere del filtro. Se il primo carattere è <, ma il filtro non è effettivamente un frammento XML, è necessario impostare questo flag. Un filtro nel formato seguente, ad esempio, richiede l'impostazione di **WSManFlagNonXmlText** in modo che il filtro venga interpretato correttamente:

`<25 && > 1`

Se il filtro è un frammento XML, questo flag non è necessario perché il frammento inizia con <, che WinRM interpreta correttamente come XML. Ad esempio,

`<filter>select * from aDataStructure</filter>`

Se il filtro è in testo normale che non inizia con <, questo flag non è obbligatorio. Ad esempio,

`select * from aDataStructure`

Il metodo di scripting associato è [**WSMan. EnumerationFlagNonXmlText**](wsman-enumerationflagnonxmltext.md) e il metodo C++ è [**IWSManEx. EnumerationFlagNonXmlText**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagnonxmltext).


</dt> </dl> </dd> <dt>

<span id="EnumerationFlagReturnEPR"></span><span id="enumerationflagreturnepr"></span><span id="ENUMERATIONFLAGRETURNEPR"></span>**EnumerationFlagReturnEPR**
</dt> <dd> <dl> <dt>

2 (0x2)
</dt> <dt>



I batch contengono riferimenti a endpoint (EPRs) per le istanze XML corrispondenti, ma non le istanze effettive.

Il metodo di scripting associato è [**WSMan. EnumerationFlagReturnEPR**](wsman-enumerationflagreturnepr.md) e il metodo C++ è [**IWSManEx. EnumerationFlagReturnEPR**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnepr).


</dt> </dl> </dd> <dt>

<span id="WSManFlagReturnObjectAndEPR"></span><span id="wsmanflagreturnobjectandepr"></span><span id="WSMANFLAGRETURNOBJECTANDEPR"></span>**WSManFlagReturnObjectAndEPR**
</dt> <dd> <dl> <dt>

4 (0x4)
</dt> <dt>



I batch contengono sia le istanze XML richieste che i EPRs corrispondenti contenuti in un elemento [*WSMan: Items*](windows-remote-management-glossary.md) .

Il metodo di scripting associato è [**WSMan. EnumerationFlagReturnObjectAndEPR**](wsman-enumerationflagreturnobjectandepr.md) e il metodo C++ è [**IWSManEx. EnumerationFlagReturnObjectAndEPR**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnobjectandepr).


</dt> </dl> </dd> <dt>

<span id="WSManFlagHierarchyDeep"></span><span id="wsmanflaghierarchydeep"></span><span id="WSMANFLAGHIERARCHYDEEP"></span>**WSManFlagHierarchyDeep**
</dt> <dd> <dl> <dt>

0 (0x0)
</dt> <dt>



Le istanze delle classi derivate sono incluse e sono rappresentate in base agli schemi effettivi.

Il metodo di scripting associato è [**WSMan. EnumerationFlagHierarchyDeep**](wsman-enumerationflaghierarchydeep.md) e il metodo C++ è [**IWSManEx. EnumerationFlagHierarchyDeep**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchydeep).


</dt> </dl> </dd> <dt>

<span id="WSManFlagHierarchyShallow"></span><span id="wsmanflaghierarchyshallow"></span><span id="WSMANFLAGHIERARCHYSHALLOW"></span>**WSManFlagHierarchyShallow**
</dt> <dd> <dl> <dt>

32 (0x20)
</dt> <dt>



Le istanze delle classi derivate sono escluse. Vengono visualizzate solo le istanze del tipo richiesto.

Il metodo di scripting associato è [**WSMan. EnumerationFlagHierarchyShallow**](wsman-enumerationflaghierarchyshallow.md) e il metodo C++ è [**IWSManEx. EnumerationFlagHierarchyShallow**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchyshallow).


</dt> </dl> </dd> <dt>

<span id="WSManFlagHierarchyDeepBasePropsOnly"></span><span id="wsmanflaghierarchydeepbasepropsonly"></span><span id="WSMANFLAGHIERARCHYDEEPBASEPROPSONLY"></span>**WSManFlagHierarchyDeepBasePropsOnly**
</dt> <dd> <dl> <dt>

64 (0x40)
</dt> <dt>



Le istanze delle classi derivate sono incluse e sono rappresentate in base allo schema della classe di base. Le proprietà definite nella classe derivata non vengono visualizzate.

Il metodo di scripting associato è [**WSMan. EnumerationFlagHierarchyDeepBasePropsOnly**](wsman-enumerationflaghierarchydeepbasepropsonly.md) e il metodo C++ è [**IWSManEx. EnumerationFlagHierarchyDeepBasePropsOnly**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchydeepbasepropsonly).


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                 |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                           |
| Intestazione<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti ed enumerazioni WinRM](winrm-constants-and-enumerations.md)
</dt> <dt>

[Enumerazione o elenco di tutte le istanze di una risorsa](enumerating-or-listing-all-instances-of-a-resource.md)
</dt> <dt>

[Esecuzione di query per istanze specifiche di una risorsa](querying-for-specific-instances-of-a-resource.md)
</dt> </dl>

 

 





