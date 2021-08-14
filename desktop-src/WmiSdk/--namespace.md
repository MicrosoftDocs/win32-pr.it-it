---
description: Rappresenta uno spazio dei nomi WMI.
ms.assetid: d5f0abc7-32cf-4d85-b5cd-5d60c991bcbc
ms.tgt_platform: multiple
title: __Namespace classe
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
ms.openlocfilehash: 4640570dd834b42652d04262b70ec84fac106d99f463ca22144e28ad388a0937
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118320769"
---
# <a name="__namespace-class"></a>\_\_Classe Namespace

La **\_ \_ classe di** sistema Namespace rappresenta uno spazio dei nomi WMI.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class __Namespace : __SystemClass
{
  string Name;
};
```

## <a name="members"></a>Members

La **\_ \_ classe Namespace** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **\_ \_ classe Namespace** ha queste proprietà.

<dl> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> <dt>

Qualificatori: [ **Chiave**](standard-qualifiers.md)
</dt> </dl>

Nome spazio dei nomi.

</dd> </dl>

## <a name="remarks"></a>Commenti

La **\_ \_ classe Namespace** è derivata da [**\_ \_ SystemClass**](--systemclass.md), che non ha proprietà.

È possibile usare **\_ \_ Lo spazio dei** nomi per identificare, creare ed eliminare gli spazi dei nomi figlio all'interno dello spazio dei nomi di lavoro corrente per il quale si dispone di un oggetto [**IWbemServices.**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) La creazione di una nuova istanza di **\_ \_ Namespace all'interno** di qualsiasi spazio dei nomi funzionante crea uno spazio dei nomi figlio all'interno dello spazio dei nomi funzionante. Al contrario, l'eliminazione di un'istanza di **\_ \_ Namespace rimuove** lo spazio dei nomi figlio dallo spazio dei nomi funzionante. Si noti che l'eliminazione di uno spazio dei nomi figlio elimina anche tutte le relative classi e istanze.

L'enumerazione di istanze di questa classe all'interno di qualsiasi spazio dei nomi funzionante fornisce gli spazi dei nomi figlio disponibili.

Ad esempio, all'interno dello spazio \\ dei nomi radice sono presenti due istanze dello spazio dei **\_ \_ nomi**. Uno ha la **proprietà Name** impostata su "Default", l'altro **ha Name** impostato su "Cimv2". Queste istanze rappresentano rispettivamente gli spazi dei nomi radice predefinito \\ \\ e \\ \\ cimv2 radice.

## <a name="examples"></a>Esempio

[L'esempio VBScript](https://Gallery.TechNet.Microsoft.Com/4a8e84f1-4b52-452c-ae4f-e4e00e266257) Elenca tutti gli spazi dei nomi WMI nella raccolta TechNet usa una chiamata ricorsiva per elencare tutte le istanze della classe \_ \_ Namespace in un sistema.

L'esempio di codice seguente recupera tutti gli spazi dei nomi in PowerShell.


```PowerShell
get-wmiobject __namespace -namespace 'root' -list -recurse | format-table __namespace
```



L'esempio di codice seguente migliora l'esempio precedente e aggiunge altre informazioni.


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

 

 




