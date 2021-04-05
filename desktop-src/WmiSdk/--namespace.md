---
description: Rappresenta uno spazio dei nomi WMI.
ms.assetid: d5f0abc7-32cf-4d85-b5cd-5d60c991bcbc
ms.tgt_platform: multiple
title: Classe __Namespace
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __Namespace
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 9f396b588f372f26a808e97593ffcc30eac9b3ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884781"
---
# <a name="__namespace-class"></a>\_\_Classe Namespace

La classe di sistema **\_ \_ namespace** rappresenta uno spazio dei nomi WMI.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class __Namespace : __SystemClass
{
  string Name;
};
```

## <a name="members"></a>Members

La classe **\_ \_ namespace** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **\_ \_ namespace** dispone di queste proprietà.

<dl> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [ **chiave**](standard-qualifiers.md)
</dt> </dl>

Nome spazio dei nomi.

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **\_ \_ dello spazio dei nomi** è derivata da [**\_ \_ SystemClass**](--systemclass.md), che non dispone di proprietà.

È possibile utilizzare lo **\_ \_ spazio dei nomi** per identificare, creare ed eliminare gli spazi dei nomi figlio nello spazio dei nomi funzionante corrente per il quale si dispone di un oggetto [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) . La creazione di una nuova istanza dello **\_ \_ spazio dei** nomi in qualsiasi spazio dei nomi funzionante crea uno spazio dei nomi figlio nello spazio dei nomi funzionante. Viceversa, l'eliminazione di un'istanza dello **\_ \_ spazio dei nomi** consente di rimuovere lo spazio dei nomi figlio dallo spazio dei nomi funzionante. Si noti che l'eliminazione di uno spazio dei nomi figlio elimina anche tutte le relative classi e istanze.

L'enumerazione delle istanze di questa classe in qualsiasi spazio dei nomi funzionante fornisce gli spazi dei nomi figlio disponibili.

Ad esempio, all'interno dello \\ spazio dei nomi radice si trovano due istanze dello **\_ \_ spazio dei nomi**. Una ha la proprietà **Name** impostata su "default", l'altra ha il **nome** impostato su "Cimv2". Queste istanze rappresentano \\ rispettivamente gli \\ \\ \\ spazi dei nomi predefiniti radice e CIMV2 radice.

## <a name="examples"></a>Esempio

Nell'esempio relativo all' [elenco di tutti gli spazi dei nomi WMI](https://Gallery.TechNet.Microsoft.Com/4a8e84f1-4b52-452c-ae4f-e4e00e266257) della raccolta TechNet viene utilizzata una chiamata ricorsiva per elencare tutte le istanze della \_ \_ classe dello spazio dei nomi in un sistema.

Nell'esempio di codice seguente vengono recuperati tutti gli spazi dei nomi in PowerShell.


```PowerShell
get-wmiobject __namespace -namespace 'root' -list -recurse | format-table __namespace
```



Nell'esempio di codice seguente viene migliorato l'esempio precedente e vengono aggiunte altre informazioni.


```PowerShell
# Set computer name 
$comp = "." 
 
# Get the name spaces on the local computer, and the local computer name 
$Namespace = get-wmiobject __namespace -namespace 'root' -list -recurse -computer $comp  
$hotsname = hostname 
 
# Display number of and names of the namespaces 
"{0} Namespaces on: {1}" -f $namespace.count, $hostname 
$NameSpace| sort __namespace  | Format-Table @{Expression = "__Namespace"; Label = "Namespace"}
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |
| Spazio dei nomi<br/>                | Tutti gli spazi dei nomi WMI<br/>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_\_SystemClass**](--systemclass.md)
</dt> <dt>

[Classi di sistema WMI](wmi-system-classes.md)
</dt> </dl>

 

 




