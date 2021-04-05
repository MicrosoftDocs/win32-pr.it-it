---
title: Classe MDM_Policy_Result01_ActiveXControls02
description: La \_ classe ActiveXControls02 dei criteri MDM \_ Result01 \_ rappresenta i criteri di controllo ActiveX disponibili.
ms.assetid: 46778743-59d7-4d37-836c-3f263bb8a083
keywords:
- Classe MDM_Policy_Result01_ActiveXControls02
- Classe MDM_Policy_Result01_ActiveXControls02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_ActiveXControls02
- MDM_Policy_Result01_ActiveXControls02.InstanceID
- MDM_Policy_Result01_ActiveXControls02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36ee572cfbbd823ce9e819688d9399b22f5d564c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048414"
---
# <a name="mdm_policy_result01_activexcontrols02-class"></a>\_ \_ Classe Result01 ActiveXControls02 di criteri \_ MDM

\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

La \_ classe ActiveXControls02 dei criteri MDM \_ Result01 \_ rappresenta i criteri di controllo ActiveX disponibili.

La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_ActiveXControls02
{
  string InstanceID;
  string ParentID;
  string ApprovedInstallationSites;
};
```

## <a name="members"></a>Members

La **classe \_ \_ Result01 \_ ActiveXControls02 dei criteri MDM** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ \_ \_ ActiveXControls02 dei criteri MDM Result01** ha queste proprietà.

<dl> <dt>

[ApprovedInstallationSites](/windows/client-management/mdm/policy-csp-activexcontrols#activexcontrols-approvedinstallationsites)
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows 10\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                      |
| Spazio dei nomi<br/>                | \\ \\ Dmmap MDM CIMV2 \\ radice<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



 

