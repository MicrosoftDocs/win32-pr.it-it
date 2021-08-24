---
title: MDM_Policy_User_Result01_AttachmentManager02 classe
description: La classe Mdm \_ Policy \_ User \_ Result01 \_ AttachmentManager02 rappresenta i criteri di gestione degli allegati disponibili.
ms.assetid: c6cfec0d-24f8-4356-a12b-d9b9944776a7
keywords:
- MDM_Policy_User_Result01_AttachmentManager02 classe
- MDM_Policy_User_Result01_AttachmentManager02 classe , descritta
topic_type:
- apiref
api_name:
- MDM_Policy_User_Result01_AttachmentManager02
- MDM_Policy_User_Result01_AttachmentManager02.InstanceID
- MDM_Policy_User_Result01_AttachmentManager02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d646a58cb2d8cd3330ca7f182f7b3213fe0f76479ecd94bd0a13e9d19794b163
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119750411"
---
# <a name="mdm_policy_user_result01_attachmentmanager02-class"></a>Classe \_ \_ AttachmentManager02 mdm Policy User \_ \_ Result01

\[Alcune informazioni riguardano un prodotto pre-rilasciato che può essere modificato sostanzialmente prima del rilascio in commercio. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

La classe Mdm \_ Policy \_ User \_ Result01 \_ AttachmentManager02 rappresenta i criteri di gestione degli allegati disponibili.

La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Result01_AttachmentManager02
{
  string InstanceID;
  string ParentID;
  string DoNotPreserveZoneInformation;
  string HideZoneInfoMechanism;
  string NotifyAntivirusPrograms;
};
```

## <a name="members"></a>Members

La **classe MDM Policy User \_ \_ \_ Result01 \_ AttachmentManager02** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Mdm Policy User \_ \_ \_ Result01 \_ AttachmentManager02** ha queste proprietà.

<dl> <dt>

[DoNotPreserveZoneInformation](/windows/client-management/mdm/policy-csp-attachmentmanager#attachmentmanager-donotpreservezoneinformation)
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

</dd> <dt>

[HideZoneInfoMechanism](/windows/client-management/mdm/policy-csp-attachmentmanager#attachmentmanager-hidezoneinfomechanism)
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

</dd> <dt>

[NotifyAntivirusPrograms](/windows/client-management/mdm/policy-csp-attachmentmanager#attachmentmanager-notifyantivirusprograms)
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
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

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                      |
| Spazio dei nomi<br/>                | Root \\ cimv2 \\ mdm \\ dmmap<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



 

