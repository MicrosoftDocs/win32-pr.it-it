---
title: MDM_EnterpriseAPN_01 classe
description: La classe MDM EnterpriseAPN 01 viene usata dall'azienda per effettuare il \_ \_ provisioning di un APN per Internet.
ms.assetid: c5fc0a86-98b7-4d0c-aae5-be836e48eee7
keywords:
- MDM_EnterpriseAPN_01 classe
- MDM_EnterpriseAPN_01 classe, descritta
topic_type:
- apiref
api_name:
- MDM_EnterpriseAPN_01
- MDM_EnterpriseAPN_01.InstanceID
- MDM_EnterpriseAPN_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3661328e3e7d9854a2d298e2226a56838af652dc3732010baf95bd9c634f540
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104291"
---
# <a name="mdm_enterpriseapn_01-class"></a>Classe MDM \_ EnterpriseAPN \_ 01

\[Alcune informazioni riguardano prodotti pre-rilasciati che possono essere modificati in modo sostanziale prima che venga rilasciato commercialmente. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

La **classe MDM \_ EnterpriseAPN \_ 01** viene usata dall'azienda per effettuare il provisioning di un APN per Internet.

La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_EnterpriseAPN_01
{
  string  InstanceID;
  string  ParentID;
  string  APNName;
  string  IPType;
  boolean IsAttachAPN;
  string  ClassId;
  string  AuthType;
  string  UserName;
  string  Password;
  string  IccId;
  boolean AlwaysOn;
  boolean Enabled;
  string  Roaming;
};
```

## <a name="members"></a>Members

La **classe MDM \_ EnterpriseAPN \_ 01** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe MDM \_ EnterpriseAPN \_ 01** ha queste proprietà.

<dl> <dt>

[AlwaysOn](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-alwayson)
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

</dd> <dt>

[APNName](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-apnname)
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

</dd> <dt>

[Authtype](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-authtype)
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

</dd> <dt>

[Classid](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-classid)
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

</dd> <dt>

[Enabled](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-enabled)
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

</dd> <dt>

[IccId](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-iccid)
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nome della connessione visualizzato da Windows Gestione connessioni.

</dd> <dt>

[IPType](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-iptype)
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

</dd> <dt>

[IsAttachAPN](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-isattachapn)
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

</dd> <dt>

**Parentid**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Descrive il percorso completo del nodo padre. Per questa classe, la stringa è "./Vendor/MSFT/EnterpriseAPN"

</dd> <dt>

[Password](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-password)
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

</dd> <dt>

[Roaming](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-roaming)
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

</dd> <dt>

[UserName](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-username)
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                      |
| Spazio dei nomi<br/>                | Dmmap \\ mdm cimv2 \\ \\ radice<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Uso di script di PowerShell con il provider bridge WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

