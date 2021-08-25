---
description: Una raccolta è un concetto di automazione standard che fornisce un'interfaccia uniforme a un set di oggetti su cui è possibile eseguire l'iterazione.
ms.assetid: c1ebe529-33cb-4158-923d-124d6328fc60
ms.tgt_platform: multiple
title: Accesso a una raccolta WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: da563830b742b47a138c106b21efe197108bbdddf7ad7f86b90984a04431aa0f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860515"
---
# <a name="accessing-a-wmi-collection"></a>Accesso a una raccolta WMI

Una raccolta è un concetto di automazione standard che fornisce un'interfaccia uniforme a un set di oggetti su cui è possibile eseguire l'iterazione. L'API scripting per WMI espone una serie di interfacce conformi al paradigma di raccolta. In ogni caso, usare il **metodo Item** per identificare gli elementi usando una stringa contenente il valore .

Le [**raccolte SWbemPropertySet**](swbempropertyset.md), [**SWbemQualifierSet**](swbemqualifierset.md)e [**SWbemMethodSet**](swbemmethodset.md) vengono usate principalmente per modificare lo schema. Un [**oggetto SWbemObjectSet**](swbemobjectset.md) contiene oggetti WMI, ad esempio un'istanza [**di \_ LogicalDisk Win32,**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) ottenuti tramite chiamate, ad esempio [**SWbemServices.InstancesOf**](swbemservices-instancesof.md) o [**SWbemObject.Associaters. \_**](swbemobject-associators-.md) [**L'oggetto SWbemRefresher**](swbemrefresher.md) può contenere solo istanze di classi WMI. [**L'oggetto SWbemNamedValueSet**](swbemnamedvalueset.md) può contenere oggetti WMI o qualsiasi altro tipo di dati richiesto da un provider per la chiamata al metodo.

> [!Note]  
> Gli argomenti seguenti sono stati scritti principalmente per VBScript. C# usa [l'interfaccia IEnumerable](/dotnet/api/system.collections.ienumerable) standard per fascicolare ed enumerare gli oggetti. Al contrario, PowerShell usa in genere una raccolta di oggetti implicita ogni volta che un valore restituito contiene più risultati.

 

Nella tabella seguente sono elencate le raccolte nell'API scripting per WMI e gli elementi e i parametri per ogni raccolta.



| Raccolta                                       | Elemento                                              | Parametro Item()                                                         |
|--------------------------------------------------|------------------------------------------------------|--------------------------------------------------------------------------|
| [**SWbemObjectSet**](swbemobjectset.md)         | [**SWbemObject**](swbemobject.md)                   | Percorso dell'oggetto                                                              |
| [**SWbemPropertySet**](swbempropertyset.md)     | [**Proprietà SWbemProperty**](swbemproperty.md)               | Nome proprietà                                                            |
| [**SWbemQualifierSet**](swbemqualifierset.md)   | [**SWbemQualifier**](swbemqualifier.md)             | Nome qualificatore                                                           |
| [**SWbemMethodSet**](swbemmethodset.md)         | [**SWbemMethod**](swbemmethod.md)                   | Nome metodo                                                              |
| [**SWbemNamedValueSet**](swbemnamedvalueset.md) | [**SWbemNamedValue**](swbemnamedvalue.md)           | Nome del valore                                                               |
| [**SWbemPrivilegeSet**](swbemprivilegeset.md)   | [**SWbemPrivilege**](swbemprivilege.md)             | Nome del privilegio                                                           |
| [**SWbemRefresher**](swbemrefresher.md)         | [**SWbemRefreshableItem**](swbemrefreshableitem.md) | Indice dell'elemento [**nell'oggetto SWbemRefresher**](swbemrefresher.md) |



 

Per altre informazioni ed esempi di aggiunta e rimozione [](removing-a-single-item-from-a-collection.md) di elementi da una raccolta, vedere Rimozione di un singolo elemento da una raccolta e Rimozione di più elementi [da una raccolta](removing-multiple-items-from-a-collection.md). Per altre informazioni sull'uso delle classi, vedere [Modifica delle informazioni sulle classi e sulle istanze](manipulating-class-and-instance-information.md).

 

 
