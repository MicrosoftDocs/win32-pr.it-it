---
title: MDM_VPNv2_APNBinding02 classe
description: Riservato per usi futuri. | MDM_VPNv2_APNBinding02 classe
ms.assetid: ef530e79-b9cc-4bee-8d7b-45227ed55dbe
keywords:
- MDM_VPNv2_APNBinding02 classe
- MDM_VPNv2_APNBinding02 classe , descritta
topic_type:
- apiref
api_name:
- MDM_VPNv2_APNBinding02
- MDM_VPNv2_APNBinding02.InstanceID
- MDM_VPNv2_APNBinding02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff62d5a2280a28292289e6e6a1374615f066a66463eef9a8c0e3db58383874ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084811"
---
# <a name="mdm_vpnv2_apnbinding02-class"></a>Classe MDM \_ VPNv2 \_ APNBinding02

\[Alcune informazioni riguardano un prodotto pre-rilasciato che può essere modificato sostanzialmente prima del rilascio in commercio. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

Riservato per uso futuro

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_APNBinding02
{
  string  InstanceID;
  string  ParentID;
  string  ProviderId;
  string  AccessPointName;
  string  UserName;
  string  Password;
  boolean IsCompressionEnabled;
  string  AuthenticationType;
};
```

## <a name="members"></a>Members

La **classe MDM \_ VPNv2 \_ APNBinding02** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe MDM \_ VPNv2 \_ APNBinding02** ha queste proprietà.

<dl> <dt>

[AccessPointName](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-apnbinding-accesspointname)
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

</dd> <dt>

[Authenticationtype](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-apnbinding-authenticationtype)
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Riservato per utilizzi futuri.

</dd> <dt>

[IsCompressionEnabled](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-apnbinding-iscompressionenabled)
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

</dd> <dt>

**Parentid**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Riservato per utilizzi futuri.

</dd> <dt>

[Password](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-apnbinding-password)
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

</dd> <dt>

[ProviderId](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-apnbinding-providerid)
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

</dd> <dt>

[UserName](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-apnbinding-username)
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
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

[Uso di script di PowerShell con il provider Bridge WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

