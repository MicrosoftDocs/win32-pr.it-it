---
description: Un oggetto SWbemPropertySet è una raccolta di oggetti SWbemProperty.
ms.assetid: 0edad17b-facc-4885-9ce4-561ca6f57a66
ms.tgt_platform: multiple
title: Oggetto SWbemPropertySet (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPropertySet
- ISWbemPropertySet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 05ae5d5e0bfbc5ab0733e00e4649baa2849d3446
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318498"
---
# <a name="swbempropertyset-object"></a>Oggetto SWbemPropertySet

Un oggetto **SWbemPropertySet** è una raccolta di oggetti [**SWbemProperty**](swbemproperty.md) . È possibile aggiungere elementi alla raccolta usando il metodo [**Add**](swbempropertyset-add.md) , recuperare gli elementi dalla raccolta usando il metodo [**Item**](swbempropertyset-item.md) e rimuovere gli elementi dalla raccolta usando il metodo [**Remove**](swbempropertyset-remove.md) . Per ulteriori informazioni, vedere [accesso a una raccolta](accessing-a-collection.md). Questo oggetto non può essere creato dalla chiamata [CreateObject](creating-an-object-using-vbscript.md) di VBScript.

Gli oggetti [**SWbemProperty**](swbemproperty.md) che costituiscono una raccolta **SWbemPropertySet** vengono utilizzati per descrivere le proprietà di una singola istanza o classe WMI.

## <a name="members"></a>Membri

L'oggetto **SWbemPropertySet** dispone di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'oggetto **SWbemPropertySet** dispone di questi metodi.



| Metodo                                    | Descrizione                                                                                                                     |
|:------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------|
| [**Aggiungere**](swbempropertyset-add.md)       | Aggiunge un oggetto [**SWbemProperty**](swbemproperty.md) alla raccolta **SWbemPropertySet** .<br/>                        |
| [**Elemento**](swbempropertyset-item.md)     | Ottiene un oggetto denominato [**SWbemProperty**](swbemproperty.md) dalla raccolta. Questo è il metodo predefinito per questo oggetto.<br/> |
| [**Rimuovi**](swbempropertyset-remove.md) | Elimina un oggetto [**SWbemProperty**](swbemproperty.md) dalla raccolta.<br/>                                        |



 

### <a name="properties"></a>Proprietà

L'oggetto **SWbemPropertySet** dispone di queste proprietà.



| Proprietà                                           | Tipo di accesso          | Descrizione                                                            |
|:---------------------------------------------------|:---------------------|:-----------------------------------------------------------------------|
| [**Conteggio**](swbempropertyset-count.md)<br/> | Sola lettura<br/> | Numero di elementi nella raccolta **SWbemPropertySet** .<br/> |



 

## <a name="examples"></a>Esempio

Nell'esempio VBScript seguente viene illustrato come [**SWbemPropertySet. Remove**](swbempropertyset-remove.md) può restituire **wbemErrResetToDefault** se la proprietà viene sottoposta a override.


```VB
on error resume next 

'Create a keyed class with a defaulted property
set service = GetObject("Winmgmts:")
set emptyclass = service.Get
emptyclass.path_.class = "REMOVETEST00"
set prop = emptyclass.properties_.add ("p", 19)

prop.qualifiers_.add "key", true
emptyclass.properties_.add ("q", 19).Value = 12

emptyclass.put_

'create an instance and override the property
set instance = service.get ("RemoveTest00").spawninstance_

instance.properties_("q").Value = 24
instance.properties_("p").Value = 1
instance.put_

'retrieve the instance and remove the property
set instance = service.get ("removetest00=1")
set property = instance.properties_ ("q")

WScript.echo "Overridden value of property is [24]:", property.value
WScript.echo ""

instance.properties_.remove "q"
set property = instance.properties_ ("q")
WScript.echo "Value of property after removal is [12]:", property.value
WScript.echo ""

if err <> 0 then
 WScript.Echo "0x" & Hex(Err.Number), Err.Description, Err.Source
end if
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMPROPERTYSET CLSID<br/>                                                      |
| IID<br/>                      | \_ISWBEMPROPERTYSET IID<br/>                                                       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti API di scripting](scripting-api-objects.md)
</dt> </dl>

 

 




