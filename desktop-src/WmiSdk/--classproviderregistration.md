---
description: Registra i provider di classi in WMI.
ms.assetid: 1af7d9ed-c5e4-47e4-839d-53d579ef7cea
ms.tgt_platform: multiple
title: Classe __ClassProviderRegistration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ClassProviderRegistration
- All
- All
- All
- All
- All
- All
- All
- All
- All
- All
- All
- All
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 32442122624035ec376bed3be8b3ef20c80f8524
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760460"
---
# <a name="__classproviderregistration-class"></a>\_\_Classe ClassProviderRegistration

La classe di sistema **\_ \_ ClassProviderRegistration** registra i provider di classi in WMI.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class __ClassProviderRegistration : __ObjectProviderRegistration
{
  boolean        SupportsBatching;
  datetime       CacheRefreshInterval;
  sint32         InteractionType = 0;
  __Provider REF provider;
  boolean        PerUserSchema;
  string         QuerySupportLevels[];
  string         ReferencedSetQueries[];
  string         ResultSetQueries[];
  boolean        ReSynchroniseOnNamespaceOpen;
  boolean        SuppportsBatching;
  boolean        SupportsEnumeration = False;
  boolean        SupportsDelete = False;
  boolean        SupportsGet = False;
  boolean        SupportsPut = False;
  boolean        SupportsTransactions;
  string         UnsupportedQueries[];
  uint32         Version;
};
```

## <a name="members"></a>Members

La classe **\_ \_ ClassProviderRegistration** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **\_ \_ ClassProviderRegistration** dispone di queste proprietà.

<dl> <dt>

**CacheRefreshInterval**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Non usato.

</dd> <dt>

**InteractionType**
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Indica se il provider di classi o istanze fornisce dati oppure si basa su WMI e sul repository Common Information Model (CIM). I provider Pull supportano l'accesso dinamico ai dati e i provider di push archiviano i dati nel repository CIM e si basano su WMI per fornire l'accesso. Il valore predefinito è 0 (zero). Questa proprietà viene ereditata da [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md). Per ulteriori informazioni, vedere [determinare lo stato di push o pull](determining-push-or-pull-status.md).

<dt>

<span id="Pull"></span><span id="pull"></span><span id="PULL"></span>

<span id="Pull"></span><span id="pull"></span><span id="PULL"></span>**Pull** (0)


</dt> <dd>

Il provider è un provider di pull.

</dd> <dt>

<span id="Push"></span><span id="push"></span><span id="PUSH"></span>

<span id="Push"></span><span id="push"></span><span id="PUSH"></span>**Push** (1)


</dt> <dd>

Il provider è un provider di push.

</dd> <dt>

<span id="PushVerify"></span><span id="pushverify"></span><span id="PUSHVERIFY"></span>

<span id="PushVerify"></span><span id="pushverify"></span><span id="PUSHVERIFY"></span>**PushVerify** (2)


</dt> <dd>

Il provider è un provider di verifica push. Si noti che al momento i provider **PushVerify** non sono supportati.

</dd> </dl>

</dd> <dt>

**PerUserSchema**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Non usato.

</dd> <dt>

**provider**
</dt> <dd> <dl> <dt>

Tipo di dati: **\_ \_ provider**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Percorso dell'oggetto a un provider di classi. Questa proprietà viene ereditata da [**\_ \_ ProviderRegistration**](--providerregistration.md).

</dd> <dt>

**QuerySupportLevels**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Matrice dei tipi di supporto incluso nel provider per l'elaborazione delle query. Questa proprietà viene ereditata da [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md). I provider di classi sono necessari per supportare almeno un tipo di query. I provider di istanze possono impostare **QuerySupportLevels** su **null** se non supportano l'elaborazione delle query. I provider che supportano le query implementano il metodo [**IWbemServices:: ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) e impostano questa proprietà su uno o più dei valori seguenti:

<dt>



 ("WQL: UnarySelect")


</dt> <dd></dd> <dt>



 ("WQL: References")


</dt> <dd></dd> <dt>



 ("WQL: Associrs")


</dt> <dd></dd> <dt>



 ("WQL: V1ProviderDefined")


</dt> <dd></dd> </dl>

</dd> <dt>

**ReferencedSetQueries**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Una o più query che descrivono il set di classi di riferimento supportate da un provider di classi. I provider che possono fornire classi di associazione devono includere almeno una query in questa proprietà.

</dd> <dt>

**ResultSetQueries**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Una o più query che descrivono il set di tutte le classi che possono essere fornite dal provider di classi o un superset di tali classi. Questa proprietà non specifica mai un subset di classi supportate.

</dd> <dt>

**ReSynchroniseOnNamespaceOpen**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Non usato.

</dd> <dt>

**SupportsBatching**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Non usato.

Questa proprietà viene ereditata da [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md).

</dd> <dt>

**SupportsDelete**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Se **true**, il provider supporta l'eliminazione dei dati. Questa proprietà viene ereditata da [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md).

<dt>



 True


</dt> <dd>

Il provider supporta l'eliminazione di una classe o di un'istanza implementando uno dei [**IWbemServices::D eleteclassasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) (provider di classi) o [**IWbemServices::D eleteinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) (provider di istanze).

</dd> <dt>



 False


</dt> <dd>

Il provider non supporta l'eliminazione dei dati e restituisce **il \_ provider WBEM e \_ non è \_ \_ in grado** di [**DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) o [**DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync).

</dd> </dl>

</dd> <dt>

**SupportsEnumeration**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Se **true**, il provider supporta l'enumerazione dei dati. Questa proprietà viene ereditata da [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md).

<dt>



 True


</dt> <dd>

Il provider supporta l'enumerazione dei dati implementando uno dei [**IWbemServices:: CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) (provider di classi) o [**IWbemServices:: CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) (provider di istanze).

</dd> <dt>



 False


</dt> <dd>

Il provider non supporta l'enumerazione dei dati e restituisce **il \_ provider WBEM e \_ non è \_ \_ in grado** di [**CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) o [**CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync).

</dd> </dl>

</dd> <dt>

**SupportsGet**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Se **true**, il provider di classi o istanze supporta il recupero dei dati. Questa proprietà viene ereditata da [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md).

<dt>



 True


</dt> <dd>

Il provider supporta il recupero dei dati mediante l'implementazione di [**IWbemServices:: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).

</dd> <dt>



 False


</dt> <dd>

Il provider non supporta il recupero dei dati e restituisce il **\_ provider WBEM \_ e \_ non \_ idoneo** per [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).

</dd> </dl>

</dd> <dt>

**SupportsPut**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Se **true**, la classe o il provider di istanze supporta la modifica dei dati. Questa proprietà viene ereditata da [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md).

<dt>



 True


</dt> <dd>

Il provider supporta la modifica della classe o dell'istanza implementando uno dei [**IWbemServices::P utclassasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) (provider di classi) o [**IWbemServices::P utinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) (provider di classi).

</dd> <dt>



 False


</dt> <dd>

Il provider non supporta la modifica dei dati e restituisce il **\_ provider WBEM e \_ \_ non \_ idoneo** per [**PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) o [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync).

</dd> </dl>

</dd> <dt>

**SupportsTransactions**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Non usato.

</dd> <dt>

**SuppportsBatching**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Non usato.

</dd> <dt>

**UnsupportedQueries**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Una o più query che descrivono il set di classi non supportate dal provider di classi. Utilizzare questa proprietà per sottrarre dal set di classi implicito da **ResultSetQueries**.

</dd> <dt>

**Versione**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Versione del provider di classi.

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **\_ \_ ClassProviderRegistration** deriva da [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md), derivata da [**\_ \_ ProviderRegistration**](--providerregistration.md).

Le proprietà ereditate da [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md) indicano se il provider di classi supporta il recupero, la modifica, l'eliminazione, l'enumerazione e l'elaborazione di query dei dati. La proprietà **InteractionType** specifica se il provider di classi è o meno progettato come provider pull o push. Per ulteriori informazioni, vedere [determinare lo stato di push o pull](determining-push-or-pull-status.md).

La classe [**\_ \_ ProviderRegistration**](--providerregistration.md) definisce la proprietà del [**provider**](/windows/desktop/api/Provider/nl-provider-provider) . Solo gli amministratori possono registrare un provider creando un'istanza di [**\_ \_ Win32Provider**](--win32provider.md) e **\_ \_ ClassProviderRegistration**. Solo gli amministratori possono eliminare un provider.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |
| Spazio dei nomi<br/>                | Tutti gli spazi dei nomi WMI<br/>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_\_ObjectProviderRegistration**](/windows/desktop/WmiSdk/--objectproviderregistration)
</dt> <dt>

[Classi di sistema WMI](wmi-system-classes.md)
</dt> <dt>

[Registrazione di un provider di classi](registering-a-class-provider.md)
</dt> <dt>

[Registrazione di un provider di istanze](registering-an-instance-provider.md)
</dt> <dt>

[**\_\_Win32Provider**](--win32provider.md)
</dt> </dl>

 

