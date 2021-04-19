---
description: La proprietà Qualifiers \_ dell'oggetto SWbemObject restituisce un oggetto dell'SWbemQualifierSet che è una raccolta di qualificatori per la classe o l'istanza corrente. Questa proprietà è di sola lettura.
ms.assetid: 5ecae751-0d83-4ad6-9840-ef47f76b1ff6
ms.tgt_platform: multiple
title: Proprietà SWbemObject.Qualifiers_ (wbemdisp. h)
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
ms.openlocfilehash: f9526596b7ae4a387cd0751ad95aff3b97dcc817
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309818"
---
# <a name="swbemobjectqualifiers_-property"></a>SWbemObject. Qualifiers ( \_ proprietà)

La proprietà **Qualifiers \_** dell'oggetto [**SWbemObject**](swbemobject.md) restituisce un oggetto [**dell'SWbemQualifierSet**](swbemqualifierset.md) che è una raccolta di qualificatori per la classe o l'istanza corrente. Questa proprietà è di sola lettura.

Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```VB
SWbemObject.Qualifiers_ As Object
```



## <a name="property-value"></a>Valore proprietà

## <a name="examples"></a>Esempio

L' [elenco tutti i qualificatori per un](https://Gallery.TechNet.Microsoft.Com/fe7a7ae2-d9d9-4c0f-bbf5-c9c112e90983) esempio di codice VBScript della classe WMI nella raccolta TechNet usa la \_ Proprietà Qualifier per elencare i qualificatori di classe per una classe WMI specificata.

L'esempio di codice [elenco tutte le classi astratte in WMI](https://Gallery.TechNet.Microsoft.Com/2eb0a3ba-d825-432e-b011-7c6fe358707f) VBScript nella raccolta TechNet elenca tutte le classi astratte WMI definite nello \\ spazio dei nomi CIMV2 radice.

L'esempio [List all Dynamic Classes in WMI](https://Gallery.TechNet.Microsoft.Com/8352ca94-264c-43c7-9dda-258d65ac6c8c) VBScript code usa la \_ Proprietà Qualifier per elencare tutte le classi dinamiche WMI (incluse le classi Association) definite nello \\ spazio dei nomi CIMV2 radice.

L'esempio di codice [Get-WritableWMIProperties.ps1](https://Gallery.TechNet.Microsoft.Com/816fb8b6-cdcf-4156-a9a3-a852ce1d2baa) PowerShell nella raccolta TechNet elenca tutte le proprietà scrivibili nello spazio dei nomi specificato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMOBJECT CLSID<br/>                                                           |
| IID<br/>                      | \_ISWBEMOBJECT IID<br/>                                                            |



 

 




