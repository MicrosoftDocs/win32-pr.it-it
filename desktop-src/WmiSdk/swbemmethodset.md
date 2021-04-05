---
description: Un oggetto SWbemMethodSet è una raccolta di oggetti SWbemMethod. Gli elementi vengono recuperati utilizzando il metodo dell'elemento. Per ulteriori informazioni, vedere Accesso a una raccolta. Questo oggetto non può essere creato dalla chiamata CreateObject di VBScript.
ms.assetid: 0ca2601f-ed40-472e-b4f2-eee750c8c8d1
ms.tgt_platform: multiple
title: Oggetto SWbemMethodSet (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemMethodSet
- ISWbemMethodSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: d47c4dc8335077d6f8568be4b56200558942ac39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882306"
---
# <a name="swbemmethodset-object"></a>Oggetto SWbemMethodSet

Un oggetto **SWbemMethodSet** è una raccolta di oggetti [**SWbemMethod**](swbemmethod.md) . Gli elementi vengono recuperati utilizzando il metodo dell' [**elemento**](swbemmethodset-item.md) . Per ulteriori informazioni, vedere [accesso a una raccolta](accessing-a-collection.md). Questo oggetto non può essere creato dalla chiamata **CreateObject** di VBScript.

> [!Note]  
> In questa versione dell'API, l'accesso in scrittura alle informazioni sul metodo non è supportato. Se si desidera definire metodi o modificare definizioni di metodo esistenti, è possibile definire le modifiche al metodo in un file MOF e inviare le modifiche utilizzando il compilatore MOF. In alternativa, usare l'API COM WMI.

 

## <a name="members"></a>Membri

L'oggetto **SWbemMethodSet** dispone di questi tipi di membri:

-   [Metodi](#swbemmethodset-object)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'oggetto **SWbemMethodSet** dispone di questi metodi.



| Metodo                              | Descrizione                                                                                                                                  |
|:------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [**Elemento**](swbemmethodset-item.md) | Recupera un oggetto [**SWbemMethod**](swbemmethod.md) dalla raccolta. Si tratta del metodo di automazione predefinito di questo oggetto.<br/> |



 

### <a name="properties"></a>Proprietà

L'oggetto **SWbemMethodSet** dispone di queste proprietà.



| Proprietà                                         | Tipo di accesso          | Descrizione                                       |
|:-------------------------------------------------|:---------------------|:--------------------------------------------------|
| [**Conteggio**](swbemmethodset-count.md)<br/> | Sola lettura<br/> | Numero di elementi nella raccolta.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMMETHODSET CLSID<br/>                                                        |
| IID<br/>                      | \_ISWBEMMETHODSET IID<br/>                                                         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti API di scripting](scripting-api-objects.md)
</dt> </dl>

 

 




