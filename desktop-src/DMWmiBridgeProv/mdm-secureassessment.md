---
title: Classe MDM_SecureAssessment
description: Il \_ SECUREASSESSMENTCLASS MDM viene usato per fornire informazioni di configurazione per il browser di valutazione sicura.
ms.assetid: ad456f01-c77d-428b-a8bf-03e9ae106e60
keywords:
- Classe MDM_SecureAssessment
- Classe MDM_SecureAssessment, descritta
topic_type:
- apiref
api_name:
- MDM_SecureAssessment
- MDM_SecureAssessment.InstanceID
- MDM_SecureAssessment.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: deef2c8ee832a54775ae9dd51d85414a607ca8b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963789"
---
# <a name="mdm_secureassessment-class"></a>MDM \_ SecureAssessment (classe)

\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

La classe **MDM \_ SecureAssessment** viene utilizzata per fornire informazioni di configurazione per il browser Secure assessment.

La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_SecureAssessment
{
  string  InstanceID;
  string  ParentID;
  string  LaunchURI;
  string  TesterAccount;
  boolean AllowTextSuggestions;
  boolean RequirePrinting;
  boolean AllowScreenMonitoring;
};
```

## <a name="members"></a>Members

La classe **MDM \_ SecureAssessment** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **MDM \_ SecureAssessment** ha queste proprietà.

<dl> <dt>

[AllowScreenMonitoring](/windows/client-management/mdm/secureassessment-csp#allowscreenmonitoring)
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[AllowTextSuggestions](/windows/client-management/mdm/secureassessment-csp#AllowTextSuggestions)
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
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

Identifica il nome del nodo padre. Per questa classe la stringa è "SecureAssessment".

</dd> <dt>

[LaunchURI](/windows/client-management/mdm/secureassessment-csp#launchuri)
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
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

Descrive il percorso completo del nodo padre. Per questa classe la stringa è "./Vendor/MSFT/"

</dd> <dt>

[RequirePrinting](/windows/client-management/mdm/secureassessment-csp#requireprinting)
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[TesterAccount](/windows/client-management/mdm/secureassessment-csp#testeraccount)
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows 10\]<br/>                                                          |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                            |
| Spazio dei nomi<br/>                | \\ \\ Dmmap MDM CIMV2 \\ radice<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv1. mof</dt> </dl>      |
| DLL<br/>                      | <dl> <dt>\\DMWmiBridgeProv.dllfile MOF</dt> </dl> |



 

