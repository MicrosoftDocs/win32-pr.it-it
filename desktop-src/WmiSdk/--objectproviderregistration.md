---
description: Funge da classe padre per le classi utilizzate per registrare i provider di classi e istanze in WMI.
ms.assetid: f7c569be-8927-42a4-b96a-abe4b7e3e23c
ms.tgt_platform: multiple
title: Classe __ObjectProviderRegistration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ObjectProviderRegistration
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
ms.openlocfilehash: a60b24278fb235cec38c127e7ebbbb481e49a140
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104345901"
---
# <a name="__objectproviderregistration-class"></a>\_\_Classe ObjectProviderRegistration

La classe di sistema astratta **\_ \_ ObjectProviderRegistration** funge da classe padre per le classi utilizzate per registrare i provider di classi e istanze in WMI.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[abstract]
class __ObjectProviderRegistration : __ProviderRegistration
{
  sint32         InteractionType = 0;
  __Provider REF provider;
  string         QuerySupportLevels[];
  boolean        SupportsBatching;
  boolean        SupportsDelete = False;
  boolean        SupportsEnumeration = False;
  boolean        SupportsGet = False;
  boolean        SupportsPut = False;
  boolean        SupportsTransactions;
};
```

## <a name="members"></a>Members

La classe **\_ \_ ObjectProviderRegistration** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **\_ \_ ObjectProviderRegistration** dispone di queste proprietà.

<dl> <dt>

**InteractionType**
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Indica se il provider di classi o istanze fornisce i propri dati oppure si basa su WMI e sul repository Common Information Model (CIM). I provider Pull supportano l'accesso dinamico ai dati e i provider di push archiviano i dati nel repository CIM e si basano su WMI per fornire l'accesso. Per ulteriori informazioni, vedere [determinare lo stato di push o pull](determining-push-or-pull-status.md). Il valore predefinito è 0 (zero).

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

Il provider è un provider di verifica push. Si noti che la verifica push non è supportata in questo momento.

</dd> </dl>

</dd> <dt>

**provider**
</dt> <dd> <dl> <dt>

Tipo di dati: **\_ \_ provider**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Riferimento a un'istanza del [**\_ \_ provider**](--provider.md) che rappresenta il percorso di un oggetto del provider di oggetti. Questa proprietà viene ereditata da [**\_ \_ ProviderRegistration**](--providerregistration.md).

</dd> <dt>

**QuerySupportLevels**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Matrice dei tipi di supporto incluso nel provider per l'elaborazione delle query. I provider di classi non supportano alcun tipo di query. I provider di istanze possono impostare **QuerySupportLevels** su **null** se non supportano l'elaborazione delle query. I provider che supportano le query implementano il metodo [**IWbemServices:: ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) e impostano questa proprietà su uno o più dei valori seguenti (il tipo di proprietà è una matrice).

"WQL: UnarySelect"

"WQL: References"

"WQL: Associatisti"

"WQL: V1ProviderDefined"

</dd> <dt>

**SupportsBatching**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Non usato.

</dd> <dt>

**SupportsDelete**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Se **true**, il provider supporta l'eliminazione dei dati.

<dt>

Vero
</dt> <dd>

Il provider supporta l'eliminazione di una classe o di un'istanza implementando uno dei [**IWbemServices::D eleteclassasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) (provider di classi) o [**IWbemServices::D eleteinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) (provider di istanze).

</dd> <dt>

Falso
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

Se **true**, il provider supporta l'enumerazione dei dati.

<dt>

Vero
</dt> <dd>

Il provider supporta l'enumerazione dei dati implementando uno dei [**IWbemServices:: CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) (provider di classi) o [**IWbemServices:: CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) (provider di istanze).

</dd> <dt>

Falso
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

Se **true**, il provider di classi o istanze supporta il recupero dei dati.

<dt>

Vero
</dt> <dd>

Il provider supporta il recupero dei dati mediante l'implementazione di [**IWbemServices:: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).

</dd> <dt>

Falso
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

Se **true**, la classe o il provider di istanze supporta la modifica dei dati.

<dt>

Vero
</dt> <dd>

Il provider supporta la modifica della classe o dell'istanza implementando uno dei [**IWbemServices::P utclassasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) (provider di classi) o [**IWbemServices::P utinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) (provider di classi).

</dd> <dt>

Falso
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

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **\_ \_ ObjectProviderRegistration** deriva da [**\_ \_ ProviderRegistration**](--providerregistration.md).

I provider di classi devono impostare la proprietà **SupportsEnumeration** su **true** perché i provider devono essere in grado di fornire WMI con un elenco delle relative classi. Se un provider di classi tenta di impostare questa proprietà su **false**, WMI contrassegna la registrazione come non valida. I provider di istanze non devono supportare l'enumerazione e possono scegliere di impostare **SupportsEnumeration** su **true** o **false**.

Un provider che imposta **QuerySupportLevels** su "WQL: UnarySelect" può accettare una query costituita dall'istruzione SELECT di base come supportata nella versione 1,0 di WMI. È previsto che i provider di classi e istanze siano in grado di gestire la proprietà di sistema della **\_ \_ classe** . Sono previsti anche provider di classi per elaborare la proprietà di sistema della **\_ \_ superclasse** e l'operatore ISA. L'operatore ISA viene utilizzato per espandere un set di risultati in classi derivate. Se a un provider viene assegnata una query che non è in grado di interpretare, viene richiesto che WMI la gestisca restituendo il valore di errore **WBEM \_ E \_ troppo \_ complesso** . Per una descrizione della sintassi WQL valida, vedere [esecuzione di query con WQL](querying-with-wql.md).

Un provider che imposta **QuerySupportLevels** su **WQL: V1ProviderDefined** può provare a supportare un set più ampio della sintassi SQL a proprio rischio, ad esempio la `ORDER BY` clausola. WMI non interpreta le clausole aggiuntive o tenta di verificare che il set di risultati sia corretto.

Solo gli amministratori possono registrare o eliminare un provider creando un'istanza di [**\_ \_ Win32Provider**](--win32provider.md) e registrando tale provider.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |
| Spazio dei nomi<br/>                | Tutti gli spazi dei nomi WMI<br/>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_\_ProviderRegistration**](/windows/desktop/WmiSdk/--providerregistration)
</dt> <dt>

[Classi di sistema WMI](wmi-system-classes.md)
</dt> <dt>

[Registrazione di un provider](registering-a-provider.md)
</dt> </dl>

 

