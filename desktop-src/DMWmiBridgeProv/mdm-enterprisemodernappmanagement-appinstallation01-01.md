---
title: MDM_EnterpriseModernAppManagement_AppInstallation01_01 classe
description: La classe MDM \_ EnterpriseModernAppManagement \_ AppInstallation01 01 viene usata per installare le app da Windows Store o da \_ un percorso ospitato.
ms.assetid: fc4c4c82-6f43-41fc-863b-940c0517f28b
keywords:
- MDM_EnterpriseModernAppManagement_AppInstallation01_01 classe
- MDM_EnterpriseModernAppManagement_AppInstallation01_01 classe , descritta
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_AppInstallation01_01
- MDM_EnterpriseModernAppManagement_AppInstallation01_01.InstanceID
- MDM_EnterpriseModernAppManagement_AppInstallation01_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d29cde4408cac13471e98d0c42b36779f8b23c0101f6ba22f383d97e181893e9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119875341"
---
# <a name="mdm_enterprisemodernappmanagement_appinstallation01_01-class"></a>Classe \_ MDM EnterpriseModernAppManagement \_ AppInstallation01 \_ 01

\[Alcune informazioni riguardano un prodotto pre-rilasciato che può essere modificato sostanzialmente prima del rilascio in commercio. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

La **classe MDM \_ EnterpriseModernAppManagement \_ AppInstallation01 \_ 01** viene usata per installare le app da Windows Store o da un percorso ospitato.

La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_EnterpriseModernAppManagement_AppInstallation01_01
{
  string InstanceID;
  string ParentID;
  sint32 LastError;
  string LastErrorDesc;
  sint32 Status;
  sint32 ProgressStatus;
};
```

## <a name="members"></a>Members

La **classe MDM \_ EnterpriseModernAppManagement \_ AppInstallation01 \_ 01** include questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe MDM \_ EnterpriseModernAppManagement \_ AppInstallation01 \_ 01** include questi metodi.



| Metodo                                                                                                    | Descrizione                                                                                                                                |
|:----------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [**HostedInstallMethod**](mdm-enterprisemodernappmanagement-appinstallation01-01-hostedinstallmethod.md) | Metodo per eseguire un'installazione di un pacchetto dell'app da un percorso ospitato (può trattarsi di un'unità locale, un'origine dati UNC o https).<br/> |
| [**StoreInstallMethod**](mdm-enterprisemodernappmanagement-appinstallation01-01-storeinstallmethod.md)   | Metodo per eseguire un'installazione di un'app e una licenza da Windows Store.<br/>                                                    |



 

### <a name="properties"></a>Proprietà

La **classe MDM \_ EnterpriseModernAppManagement \_ AppInstallation01 \_ 01** ha queste proprietà.

<dl> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identifica il nome del nodo padre. Per questa classe, la stringa è "AppInstallation".

</dd> <dt>

[LastError](/windows/client-management/mdm/enterprisemodernappmanagement-csp#appinstallation-packagefamilyname-lasterror)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

</dd> <dt>

[LastErrorDesc](/windows/client-management/mdm/enterprisemodernappmanagement-csp)
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

Descrive il percorso completo del nodo padre. Per questa classe, la stringa è "./Vendor/MSFT/EnterpriseModernAppManagement/AppInstallation"

</dd> <dt>

[Stato di avanzamento](/windows/client-management/mdm/enterprisemodernappmanagement-csp)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

</dd> <dt>

[Status](/windows/client-management/mdm/enterprisemodernappmanagement-csp#appinstallation-packagefamilyname-status)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
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

[Uso di script di PowerShell con il provider bridge WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

