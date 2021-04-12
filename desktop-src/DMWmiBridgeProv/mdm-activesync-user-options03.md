---
title: Classe MDM_ActiveSync_User_Options03
description: La \_ \_ classe Options03 dell'utente MDM ActiveSync \_ definisce le opzioni impostate per ogni account ActiveSync.
ms.assetid: b325f676-9b83-4212-a228-e2d774515be6
keywords:
- Classe MDM_ActiveSync_User_Options03
- Classe MDM_ActiveSync_User_Options03, descritta
topic_type:
- apiref
api_name:
- MDM_ActiveSync_User_Options03
- MDM_ActiveSync_User_Options03.InstanceID
- MDM_ActiveSync_User_Options03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c459e20b519801c622a091060fd6a87ced2807c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119563"
---
# <a name="mdm_activesync_user_options03-class"></a>\_ \_ Classe OPTIONS03 utente MDM ActiveSync \_

\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

La **classe \_ \_ \_ Options03 dell'utente MDM ActiveSync** definisce le opzioni impostate per ogni account ActiveSync.

La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_ActiveSync_User_Options03
{
  string InstanceID;
  string ParentID;
  string UseSSL;
  string Schedule;
  string MailAgeFilter;
  string Logging;
};
```

## <a name="members"></a>Members

La **classe \_ \_ \_ Options03 dell'utente MDM ActiveSync** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ \_ \_ Options03 dell'utente MDM ActiveSync** dispone di queste proprietà.

<dl> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identifica il nome del nodo padre.

</dd> <dt>

[Logging](/windows/client-management/mdm/activesync-csp#options-logging)
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[MailAgeFilter](/windows/client-management/mdm/activesync-csp#options-mailagefilter)
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

Descrive il percorso completo del nodo padre. Per questa classe la stringa è "./Vendor/MSFT/ActiveSync/Accounts/*GUID*/"

</dd> <dt>

[Pianificare](/windows/client-management/mdm/activesync-csp#options-schedule)
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[UseSSL](/windows/client-management/mdm/activesync-csp#options-usessl)
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
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



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilizzo di script di PowerShell con il provider del Bridge WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

