---
description: È possibile utilizzare i metodi e le proprietà dell'oggetto SWbemObject per rappresentare una definizione di classe o un'istanza dell'oggetto Strumentazione gestione Windows (WMI).
ms.assetid: d303ec1a-5e0c-4a5e-8ed3-ed353a138755
ms.tgt_platform: multiple
title: Oggetto SWbemObject (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject
- ISWbemObject
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 287395b976177170c8bdffa0e1817a8755a4d397
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309812"
---
# <a name="swbemobject-object"></a>Oggetto SWbemObject

È possibile utilizzare i metodi e le proprietà dell'oggetto **SWbemObject** per rappresentare una definizione di classe o un'istanza dell'oggetto Strumentazione gestione Windows (WMI). Questo oggetto non può essere creato dalla chiamata [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) di VBScript.

Questo oggetto supporta due tipi di proprietà e metodi. Quelli definiti in questa sezione sono proprietà e metodi generici che si applicano a tutti gli oggetti WMI. Questo oggetto espone inoltre le proprietà e i metodi dell'oggetto sottostante come proprietà e metodi di automazione dinamica di **SWbemObject**. I nomi e i tipi di tali proprietà e metodi dipendono dall'oggetto WMI sottostante. Per ulteriori informazioni sull'esposizione di queste proprietà e metodi dinamici, vedere [modifica delle informazioni sulle classi e sulle istanze](manipulating-class-and-instance-information.md).

Dal punto di vista del client WMI, questo oggetto è sempre in-process. Le operazioni di scrittura influiscono solo sulla copia locale dell'oggetto, mentre le operazioni di lettura recuperano sempre i valori dalla copia locale. Gli aggiornamenti a WMI vengono eseguiti solo quando interi oggetti vengono scritti mediante una chiamata al metodo [**SWbemObject \_ . Put**](swbemobject-put-.md) . Se si modificano le proprietà o i metodi in un oggetto **SWbemObject** , le modifiche non vengono scritte in WMI fino a quando non si chiama **SWbemObject. put \_**.

I nomi di metodo e proprietà generici definiti in questa sezione terminano sempre con un carattere di sottolineatura finale (" \_ ") per distinguerli dai metodi e dalle proprietà WMI dinamici dell'oggetto sottostante.

Si noti che non è possibile creare **SWbemObject** usando il metodo VBScript [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx). Se si desidera creare una nuova classe vuota, utilizzare [**SWbemServices. Get**](swbemservices-get.md) con un parametro path vuoto. Questa chiamata restituisce un oggetto **SWbemObject** vuoto che può diventare una classe. È quindi possibile specificare un nome di classe per la proprietà [**Class**](swbemobjectpath-class.md) dell'oggetto [**SWbemObjectPath**](swbemobjectpath.md) restituito dalla chiamata [**path \_**](swbemobject-path-.md) . Aggiungere proprietà alla nuova classe tramite il metodo [**Properties \_**](swbemobject-properties-.md) . Per creare un'istanza, chiamare **GetObject** sulla nuova classe.

Nell'esempio di codice seguente viene illustrato come ottenere una nuova classe e aggiungervi una proprietà. L'oggetto **SWbemObject** che rappresenta la classe deve essere riscritto nel repository WMI mediante una chiamata a [**put \_**](swbemobject-put-.md).


```VB
wbemCimtypeString = 8
Set objSWbemService = GetObject("Winmgmts:root\default")
Set objClass = objSWbemService.Get()
objClass.Path_.Class = "NewClass"

' Add a property
' String property
objClass.Properties_.add "PropertyName", wbemCimtypeString  
' Make the property a key property 
objClass.Properties_("PropertyName").Qualifiers_.add "key", true

' Write the new class to the root\default namespace in the repository
Set objClassPath = objClass.Put_
WScript.Echo objClassPath.Path

'Create an instance of the new class using SWbemObject.SpawnInstance
Set objNewInst = GetObject( _
    "Winmgmts:root\default:NewClass").Spawninstance_

objNewInst.PropertyName = "My Instance"

' Write the instance into the repository
Set objInstancePath = objNewInst.Put_
WScript.Echo objInstancePath.Path

```



È possibile esaminare il repository con uno strumento di visualizzazione, ad esempio [CIM Studio](further-information.md) , per verificare che la nuova classe e l'istanza vengano visualizzate. Per un esempio di rimozione di una classe e di un'istanza dal repository, vedere [**SWbemServices. Delete**](swbemservices-delete.md) o [**SWbemObject \_ . Delete**](swbemobject-delete-.md).

## <a name="members"></a>Membri

L'oggetto **SWbemObject** dispone di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'oggetto **SWbemObject** dispone di questi metodi.



| Metodo                                                        | Descrizione                                                                                             |
|:--------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [**ASSOCIATORS\_**](swbemobject-associators-.md)             | Recupera gli associatori dell'oggetto.<br/>                                                     |
| [**AssociatorsAsync\_**](swbemobject-associatorsasync-.md)   | Recupera in modo asincrono gli associatori dell'oggetto.<br/>                                      |
| [**Clone\_**](swbemobject-clone-.md)                         | Crea una copia dell'oggetto corrente.<br/>                                                          |
| [**CompareTo\_**](swbemobject-compareto-.md)                 | Verifica l'uguaglianza di due oggetti.<br/>                                                              |
| [**Delete\_**](swbemobject-delete-.md)                       | Elimina l'oggetto da WMI.<br/>                                                                 |
| [**DeleteAsync\_**](swbemobject-deleteasync-.md)             | Elimina in modo asincrono l'oggetto da WMI.<br/>                                                  |
| [**ExecMethod\_**](swbemobject-execmethod-.md)               | Esegue un metodo esportato da un provider di metodi.<br/>                                             |
| [**ExecMethodAsync\_**](swbemobject-execmethodasync-.md)     | Esegue in modo asincrono un metodo esportato da un provider di metodi.<br/>                              |
| [**GetObjectText\_**](swbemobject-getobjecttext-.md)         | Recupera la rappresentazione testuale dell'oggetto (sintassi MOF).<br/>                             |
| [**Istanze\_**](swbemobject-instances-.md)                 | Restituisce una raccolta di istanze dell'oggetto (che deve essere una classe WMI).<br/>                 |
| [**InstancesAsync\_**](swbemobject-instancesasync-.md)       | Restituisce in modo asincrono una raccolta di istanze dell'oggetto, che deve essere una classe WMI.<br/>  |
| [**Mettere\_**](swbemobject-put-.md)                             | Crea o aggiorna l'oggetto in WMI.<br/>                                                        |
| [**PutAsync\_**](swbemobject-putasync-.md)                   | Crea o aggiorna in modo asincrono l'oggetto in WMI.<br/>                                         |
| [**Riferimenti\_**](swbemobject-references-.md)               | Restituisce i riferimenti all'oggetto.<br/>                                                            |
| [**ReferencesAsync\_**](swbemobject-referencesasync-.md)     | Restituisce in modo asincrono i riferimenti all'oggetto.<br/>                                             |
| [**SpawnDerivedClass\_**](swbemobject-spawnderivedclass-.md) | Crea una nuova classe derivata dall'oggetto corrente (che deve essere una classe WMI).<br/>             |
| [**SpawnInstance\_**](swbemobject-spawninstance-.md)         | Crea una nuova istanza dell'oggetto corrente.<br/>                                              |
| [**Sottoclassi\_**](swbemobject-subclasses-.md)               | Restituisce una raccolta di sottoclassi dell'oggetto, che deve essere una classe WMI.<br/>                |
| [**SubclassesAsync\_**](swbemobject-subclassesasync-.md)     | Restituisce in modo asincrono una raccolta di sottoclassi dell'oggetto, che deve essere una classe WMI.<br/> |



 

### <a name="properties"></a>Proprietà

L'oggetto **SWbemObject** dispone di queste proprietà.



| Proprietà                                                   | Tipo di accesso          | Descrizione                                                                                                                                |
|:-----------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [**Derivazione\_**](swbemobject-derivation-.md)<br/> | Sola lettura<br/> | Contiene una matrice di stringhe che descrive la gerarchia di derivazione per la classe.<br/>                                             |
| [**Metodi\_**](swbemobject-methods-.md)<br/>       | Sola lettura<br/> | Oggetto [**SWbemMethodSet**](swbemmethodset.md) che rappresenta la raccolta di metodi per questo oggetto.<br/>                           |
| [**Percorso\_**](swbemobject-path-.md)<br/>             | Sola lettura<br/> | Contiene un oggetto [**SWbemObjectPath**](swbemobjectpath.md) che rappresenta il percorso dell'oggetto della classe o dell'istanza corrente.<br/> |
| [**Proprietà\_**](swbemobject-properties-.md)<br/> | Sola lettura<br/> | Oggetto [**SWbemPropertySet**](swbempropertyset.md) che rappresenta la raccolta di proprietà per questo oggetto.<br/>                    |
| [**Qualificatori\_**](swbemobject-qualifiers-.md)<br/> | Sola lettura<br/> | Oggetto [**dell'SWbemQualifierSet**](swbemqualifierset.md) che rappresenta la raccolta di qualificatori per questo oggetto.<br/>                  |
| [**Sicurezza\_**](swbemobject-security-.md)<br/>     | Sola lettura<br/> | Contiene un oggetto [**SWbemSecurity**](swbemsecurity.md) usato per leggere o modificare le impostazioni di sicurezza.<br/>                         |



 

## <a name="examples"></a>Esempio

L' [elenco di tutte le proprietà e i metodi di un](https://Gallery.TechNet.Microsoft.Com/f0666124-3b67-4254-8ff1-3b75ae15776d) esempio di codice VBScript della classe WMI nella raccolta TechNet utilizza SWbemObject per elencare tutti i metodi e le proprietà di una classe WMI specificata.

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



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SWbemObjectEx**](swbemobjectex.md)
</dt> <dt>

[Oggetti API di scripting](scripting-api-objects.md)
</dt> </dl>

 

