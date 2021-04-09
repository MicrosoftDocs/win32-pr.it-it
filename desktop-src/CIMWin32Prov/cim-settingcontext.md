---
description: La \_ classe CIM SettingContext associa gli oggetti di configurazione a oggetti setting.
ms.assetid: 8ed7e150-b4e6-4fd4-809b-32e870b559c4
ms.tgt_platform: multiple
title: Classe CIM_SettingContext
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SettingContext
- CIM_SettingContext.Context
- CIM_SettingContext.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 867be99e1630f02c0163516ad7a86cf84c2fac13
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966021"
---
# <a name="cim_settingcontext-class"></a>CIM \_ SettingContext (classe)

La classe **CIM \_ SettingContext** associa gli oggetti di configurazione a oggetti setting. È ad esempio possibile che le impostazioni di una scheda di rete cambino in base al sito o alla rete a cui è collegato il relativo sistema di hosting. In tal caso, il sistema informatico avrebbe due oggetti di configurazione diversi, corrispondenti alle differenze nella configurazione di rete per i due segmenti di rete. Una configurazione aggrega un oggetto Setting per la scheda di rete quando opera su un segmento. mentre l'altra configurazione aggrega un oggetto impostazione della scheda di rete diverso, specifico di un altro segmento. Si noti che molte impostazioni computer sono indipendenti dalla configurazione di rete. Entrambe le configurazioni, ad esempio, aggregano lo stesso oggetto Setting per la risoluzione del monitoraggio del sistema del computer.

> [!IMPORTANT]
> Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI. Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, UUID("{F0B752E8-DB30-11d2-85FC-0000F8102E5F}"), Aggregation, Association, AMENDMENT]
class CIM_SettingContext
{
  CIM_Configuration REF Context;
  CIM_Setting       REF Setting;
};
```

## <a name="members"></a>Members

La classe **CIM \_ SettingContext** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **CIM \_ SettingContext** dispone di queste proprietà.

<dl> <dt>

**Contesto**
</dt> <dd> <dl> <dt>

Tipo di dati **: \_ configurazione CIM**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Riferimento all'oggetto di configurazione che aggrega l'impostazione.

</dd> <dt>

**Impostazione**
</dt> <dd> <dl> <dt>

Tipo di dati **: \_ impostazione CIM**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Riferimento a un'impostazione aggregata.

</dd> </dl>

## <a name="remarks"></a>Commenti

WMI non implementa questa classe.

Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF. Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

