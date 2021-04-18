---
description: La proprietà delle impostazioni locali dell'oggetto SWbemObjectPath contiene le impostazioni locali del percorso dell'oggetto.
ms.assetid: cde4ebac-b112-48b5-a274-802e6d3fbfbf
ms.tgt_platform: multiple
title: Proprietà SWbemObjectPath. locale (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.Locale
- ISWbemObjectPath.Locale
- ISWbemObjectPath.get_Locale
- ISWbemObjectPath.put_Locale
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: a046d3dabd21b9fc46f63764f9a5c7f3e8701d36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314564"
---
# <a name="swbemobjectpathlocale-property"></a>Proprietà SWbemObjectPath. locale

La proprietà delle **impostazioni locali** dell'oggetto [**SWbemObjectPath**](swbemobjectpath.md) contiene le impostazioni locali del percorso dell'oggetto.

Quando la proprietà **SWbemObjectPath. locale** fa parte di un oggetto [**SWbemObjectPath**](swbemobjectpath.md) autonomo, è di lettura/scrittura e può essere usata per impostare il componente delle impostazioni locali del moniker.

Quando si accede alla proprietà **SWbemObjectPath. locale** come parte di una proprietà [**SWbemObject. Path \_**](swbemobject-path-.md) , è di sola lettura e restituisce il valore delle impostazioni locali utilizzate nell'associazione allo spazio dei nomi da cui è stato ottenuto l'oggetto.

Per gli identificatori delle impostazioni locali Microsoft, il formato della stringa è "MS \_ xxxx", dove xxxx è una stringa in formato esadecimale che indica il valore LCID. Ad esempio, l'identificatore delle impostazioni locali per l'inglese americano è "MS \_ 409".

Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
SWbemObjectPath.Locale As String
```



## <a name="property-value"></a>Valore proprietà

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMOBJECTPATH CLSID<br/>                                                       |
| IID<br/>                      | \_ISWBEMOBJECTPATH IID<br/>                                                        |



 

 




