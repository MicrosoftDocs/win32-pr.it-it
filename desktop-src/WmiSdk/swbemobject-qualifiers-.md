---
description: La proprietà Qualifiers \_ dell'oggetto SWbemObject restituisce un oggetto SWbemQualifierSet che è una raccolta dei qualificatori per la classe o l'istanza corrente. Questa proprietà è di sola lettura.
ms.assetid: 5ecae751-0d83-4ad6-9840-ef47f76b1ff6
ms.tgt_platform: multiple
title: SWbemObject.Qualifiers_ proprietà (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Qualifiers_
- ISWbemObject.Qualifiers_
- ISWbemObject.get_Qualifiers_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 3096b11399336a7dfcd9a36a314f6e569e24b29e8d27718345adbb55a9af0107
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119732491"
---
# <a name="swbemobjectqualifiers_-property"></a>Proprietà SWbemObject.Qualifiers \_

La **proprietà \_ Qualifiers** dell'oggetto [**SWbemObject**](swbemobject.md) restituisce un [**oggetto SWbemQualifierSet**](swbemqualifierset.md) che è una raccolta dei qualificatori per la classe o l'istanza corrente. Questa proprietà è di sola lettura.

Per una spiegazione di questa sintassi, vedere [Convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```VB
SWbemObject.Qualifiers_ As Object
```



## <a name="property-value"></a>Valore proprietà

## <a name="examples"></a>Esempio

[L'esempio di](https://Gallery.TechNet.Microsoft.Com/fe7a7ae2-d9d9-4c0f-bbf5-c9c112e90983) codice VBScript Elenca tutti i qualificatori per una classe WMI in TechNet Gallery usa la proprietà Qualifier per elencare i qualificatori di classe per una classe \_ WMI specificata.

L'esempio di codice List [All Abstract Classes in WMI](https://Gallery.TechNet.Microsoft.Com/2eb0a3ba-d825-432e-b011-7c6fe358707f) VBScript in TechNet Gallery elenca tutte le classi astratte WMI definite nello spazio dei nomi \\ cimv2 radice.

L'esempio di codice List [All Dynamic Classes in WMI](https://Gallery.TechNet.Microsoft.Com/8352ca94-264c-43c7-9dda-258d65ac6c8c) VBScript usa la proprietà Qualifier per elencare tutte le classi dinamiche WMI (incluse le classi association) definite nello spazio dei nomi \_ \\ cimv2 radice.

[LGet-WritableWMIProperties.ps1](https://Gallery.TechNet.Microsoft.Com/816fb8b6-cdcf-4156-a9a3-a852ce1d2baa) di codice di PowerShell in TechNet Gallery elenca tutte le proprietà scrivibili nello spazio dei nomi specificato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObject<br/>                                                           |
| IID<br/>                      | IID \_ ISWbemObject<br/>                                                            |



 

 




