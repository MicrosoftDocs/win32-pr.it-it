---
title: MDM_PassportForWork_Biometrics01 classe
description: La classe MDM \_ PassportForWork \_ Biometrics01 definisce le impostazioni biometriche.
ms.assetid: 64012526-eac6-4f01-8665-2bd460bc1b93
keywords:
- MDM_PassportForWork_Biometrics01 classe
- MDM_PassportForWork_Biometrics01 classe, descritta
topic_type:
- apiref
api_name:
- MDM_PassportForWork_Biometrics01
- MDM_PassportForWork_Biometrics01.InstanceID
- MDM_PassportForWork_Biometrics01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c22ecbb67499462825e1353d3d8bb8c3b08cedd93c79b1467f40f7c79ebf1f2b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084931"
---
# <a name="mdm_passportforwork_biometrics01-class"></a>Classe \_ Mdm PassportForWork \_ Biometrics01

\[Alcune informazioni riguardano prodotti pre-rilasciati che possono essere modificati in modo sostanziale prima che venga rilasciato commercialmente. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

La **classe MDM \_ PassportForWork \_ Biometrics01** definisce le impostazioni biometriche.

La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_PassportForWork_Biometrics01
{
  string  InstanceID;
  string  ParentID;
  boolean UseBiometrics;
  boolean FacialFeaturesUseEnhancedAntiSpoofing;
};
```

## <a name="members"></a>Members

La **classe MDM \_ PassportForWork \_ Biometrics01** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe MDM \_ PassportForWork \_ Biometrics01** ha queste proprietà.

<dl> <dt>

[FacialFeaturesUseEnhancedAntiSpoofing](/windows/client-management/mdm/passportforwork-csp)
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
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

Identifica il nome del nodo padre.

</dd> <dt>

**Parentid**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Descrive il percorso completo del nodo padre. Per questa classe, la stringa è "./Vendor/MSFT/PassportForWork/"

</dd> <dt>

[UseBiometrics](/windows/client-management/mdm/passportforwork-csp#usebiometrics)
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
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

 

