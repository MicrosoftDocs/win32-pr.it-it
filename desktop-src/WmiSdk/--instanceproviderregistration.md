---
description: Registra i provider di istanze in WMI.
ms.assetid: 6eba9bff-a5b9-4741-94ef-7d65b33d9aff
ms.tgt_platform: multiple
title: __InstanceProviderRegistration classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __InstanceProviderRegistration
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
ms.openlocfilehash: 773bb54ec4d132e629f21513ffa617cbe3435d35941e7c98c55810d267f614c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118821156"
---
# <a name="__instanceproviderregistration-class"></a>\_\_Classe InstanceProviderRegistration

La **\_ \_ classe di sistema InstanceProviderRegistration** registra i provider di istanze in WMI.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class __InstanceProviderRegistration : __ObjectProviderRegistration
{
  sint32         InteractionType = 0;
  __Provider REF provider;
  string         QuerySupportLevels[];
  boolean        SupportsBatching;
  boolean        SupportsDelete = False;
  boolean        SupportsEnumeration = True;
  boolean        SupportsGet = False;
  boolean        SupportsPut = False;
  boolean        SupportsTransactions;
};
```

## <a name="members"></a>Members

La **\_ \_ classe InstanceProviderRegistration** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **\_ \_ classe InstanceProviderRegistration** ha queste proprietà.

<dl> <dt>

**InteractionType**
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Indica che un provider di classi o istanze fornisce dati o recupera dati da WMI e dal repository Common Information Model (CIM). I provider di pull supportano l'accesso dinamico ai dati; e i provider push archiviano i dati nel repository CIM e usano WMI per fornirvi l'accesso. Per altre informazioni, vedere [Determinazione dello stato push o pull](determining-push-or-pull-status.md). Il valore predefinito è 0 (zero).

<dt>

<span id="Pull"></span><span id="pull"></span><span id="PULL"></span>

<span id="Pull"></span><span id="pull"></span><span id="PULL"></span>**Pull** (0)


</dt> <dd>

Provider è un provider di pull.

</dd> <dt>

<span id="Push"></span><span id="push"></span><span id="PUSH"></span>

<span id="Push"></span><span id="push"></span><span id="PUSH"></span>**Push** (1)


</dt> <dd>

Provider è un provider push.

</dd> <dt>

<span id="PushVerify"></span><span id="pushverify"></span><span id="PUSHVERIFY"></span>

<span id="PushVerify"></span><span id="pushverify"></span><span id="PUSHVERIFY"></span>**PushVerify** (2)


</dt> <dd>

Provider è un provider di verifica push. Si noti che i provider di verifica push non sono attualmente supportati.

</dd> </dl>

</dd> <dt>

**Provider**
</dt> <dd> <dl> <dt>

Tipo di dati: **\_ \_ Provider**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Riferimento a un'istanza di [**\_ \_ Provider**](--provider.md) che rappresenta il percorso dell'oggetto al provider di istanze. Questa proprietà viene ereditata da [**\_ \_ ProviderRegistration**](--providerregistration.md).

</dd> <dt>

**QuerySupportLevels**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Matrice dei tipi di supporto incluso nel provider per l'elaborazione delle query. I provider di classi non supportano tutti i tipi di query. I provider di istanze possono impostare **QuerySupportLevels** su **NULL** se non supportano l'elaborazione delle query. I provider che supportano le query implementano il metodo [**IWbemServices::ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) e impostano questa proprietà su uno o più dei valori seguenti.

<dt>



 ("WQL:UnarySelect")


</dt> <dd></dd> <dt>



 ("WQL:References")


</dt> <dd></dd> <dt>



 ("WQL:Associators")


</dt> <dd></dd> <dt>



 ("WQL:V1ProviderDefined")


</dt> <dd></dd> </dl>

</dd> <dt>

**SupportsBatching**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Non usato.

</dd> <dt>

**SupportsDelete**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Se **True,** il provider supporta l'eliminazione dei dati.

<dt>

Vero
</dt> <dd>

Il provider supporta l'eliminazione di classi o istanze implementando [**IWbemServices::D eleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) (provider di classi) o [**IWbemServices::D eleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) (provider di istanze).

</dd> <dt>

Falso
</dt> <dd>

Il provider non supporta l'eliminazione dei dati e restituisce **WBEM \_ E PROVIDER NOT \_ \_ \_ CAPABLE** da [**DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) [**o DeleteInstanceAsync.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync)

</dd> </dl>

</dd> <dt>

**SupportsEnumeration**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Se **True,** il provider supporta l'enumerazione dei dati.

<dt>



 (True)


</dt> <dd>

Il provider supporta l'enumerazione dei dati implementando uno dei metodi [**IWbemServices::CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) (provider di classi) o [**IWbemServices::CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) (provider di istanze).

</dd> <dt>



 (False)


</dt> <dd>

Il provider non supporta l'enumerazione dei dati e restituisce **WBEM \_ E PROVIDER NOT \_ \_ \_ CAPABLE** da [**CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) [**o CreateInstanceEnumAsync.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync)

</dd> </dl>

</dd> <dt>

**SupportsGet**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Se **True,** il provider di classi o istanze supporta il recupero dei dati.

<dt>

Vero
</dt> <dd>

Il provider supporta il recupero dei dati implementando [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).

</dd> <dt>

Falso
</dt> <dd>

Il provider non supporta il recupero dei dati e restituisce **WBEM \_ E PROVIDER NOT \_ \_ \_ CAPABLE** da [**GetObjectAsync.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)

</dd> </dl>

</dd> <dt>

**SupportsPut**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Se **True**, il provider di classi o istanze supporta la modifica dei dati.

<dt>



 (True)


</dt> <dd>

Il provider supporta la modifica di classi o istanze implementando uno dei metodi seguenti: [**IWbemServices::P utClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) (provider di classi) o [**IWbemServices::P utInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) (provider di classi).

</dd> <dt>



 (False)


</dt> <dd>

Il provider non supporta la modifica dei dati e restituisce **WBEM \_ E PROVIDER NOT \_ \_ \_ CAPABLE** da [**PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) [**o PutInstanceAsync.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync)

</dd> </dl>

</dd> <dt>

**SupportsTransactions**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Non usato.

</dd> </dl>

## <a name="remarks"></a>Commenti

La **\_ \_ classe InstanceProviderRegistration** è derivata da [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md), che deriva da [**\_ \_ ProviderRegistration**](--providerregistration.md). Solo gli amministratori possono registrare un provider di istanze creando un'istanza di [**\_ \_ Win32Provider**](--win32provider.md) **\_ \_ e InstanceProviderRegistration**. Solo gli amministratori possono eliminare un provider.

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
</dt> </dl>

 

