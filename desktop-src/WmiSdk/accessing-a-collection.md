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
ms.openlocfilehash: 2b875f50c1778a03c304f90c019da172be6ef5eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233474"
---
# <a name="accessing-a-wmi-collection"></a>Accesso a una raccolta WMI

Una raccolta è un concetto di automazione standard che fornisce un'interfaccia uniforme a un set di oggetti su cui è possibile eseguire l'iterazione. L'API di scripting per WMI espone una serie di interfacce conformi al paradigma della raccolta. In ogni caso, usare il metodo **Item** per identificare gli elementi usando una stringa contenente il valore.

Le raccolte [**SWbemPropertySet**](swbempropertyset.md), [**dell'SWbemQualifierSet**](swbemqualifierset.md)e [**SWbemMethodSet**](swbemmethodset.md) vengono utilizzate principalmente per modificare lo schema. Un oggetto [**SWbemObjectSet**](swbemobjectset.md) contiene oggetti WMI, ad esempio un'istanza [**Win32 \_ disco logico**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) , ottenuti tramite chiamate, ad esempio [**SWbemServices. InstancesOf**](swbemservices-instancesof.md) o [**SWbemObject. associatir \_**](swbemobject-associators-.md). L'oggetto [**SWbemRefresher**](swbemrefresher.md) può contenere solo istanze di classi WMI. L'oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) può contenere oggetti WMI o qualsiasi altro tipo di dati richiesto da un provider per la chiamata al metodo.

> [!Note]  
> Gli argomenti seguenti sono stati scritti principalmente per VBScript. C# usa l'interfaccia [IEnumerable](/dotnet/api/system.collections.ienumerable) standard per confrontare ed enumerare gli oggetti. Al contrario, PowerShell usa in genere una raccolta di oggetti implicita ogni volta che un valore restituito contiene più di un risultato.

 

Nella tabella seguente sono elencate le raccolte nell'API di scripting per WMI e gli elementi e i parametri per ogni raccolta.



| Raccolta                                       | Elemento                                              | Parametro Item ()                                                         |
|--------------------------------------------------|------------------------------------------------------|--------------------------------------------------------------------------|
| [**SWbemObjectSet**](swbemobjectset.md)         | [**SWbemObject**](swbemobject.md)                   | Percorso dell'oggetto                                                              |
| [**SWbemPropertySet**](swbempropertyset.md)     | [**SWbemProperty**](swbemproperty.md)               | Nome proprietà                                                            |
| [**Dell'SWbemQualifierSet**](swbemqualifierset.md)   | [**Oggetto SWbemQualifier**](swbemqualifier.md)             | Nome qualificatore                                                           |
| [**SWbemMethodSet**](swbemmethodset.md)         | [**SWbemMethod**](swbemmethod.md)                   | Nome metodo                                                              |
| [**SWbemNamedValueSet**](swbemnamedvalueset.md) | [**SWbemNamedValue**](swbemnamedvalue.md)           | Nome del valore                                                               |
| [**SWbemPrivilegeSet**](swbemprivilegeset.md)   | [**SWbemPrivilege**](swbemprivilege.md)             | Nome privilegio                                                           |
| [**SWbemRefresher**](swbemrefresher.md)         | [**SWbemRefreshableItem**](swbemrefreshableitem.md) | Indice dell'elemento nell'oggetto [**SWbemRefresher**](swbemrefresher.md) |



 

Per ulteriori informazioni ed esempi di aggiunta e rimozione di elementi da una raccolta, vedere [rimozione di un singolo elemento da una](removing-a-single-item-from-a-collection.md) raccolta e [rimozione di più elementi da una raccolta](removing-multiple-items-from-a-collection.md). Per ulteriori informazioni sull'utilizzo delle classi, vedere [modifica delle informazioni sulle classi e sulle istanze](manipulating-class-and-instance-information.md).

 

 
