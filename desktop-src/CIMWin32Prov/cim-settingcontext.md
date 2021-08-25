---
description: La classe CIM \_ SettingContext associa gli oggetti di configurazione agli oggetti impostazione.
ms.assetid: 8ed7e150-b4e6-4fd4-809b-32e870b559c4
ms.tgt_platform: multiple
title: CIM_SettingContext classe
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
ms.openlocfilehash: df59bff8be90d3db3ac6dfde638120779850f2691bd3e93826c57f829d034a4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919511"
---
# <a name="cim_settingcontext-class"></a>Classe \_ CiM SettingContext

La **classe CIM \_ SettingContext** associa gli oggetti di configurazione agli oggetti impostazione. Ad esempio, le impostazioni di una scheda di rete potrebbero cambiare in base al sito o alla rete a cui è collegato il sistema del computer host. In tal caso, il sistema computer avrebbe due oggetti di configurazione diversi, corrispondenti alle differenze nella configurazione di rete per i due segmenti di rete. Una configurazione aggrega un oggetto impostazione per la scheda di rete quando opera su un segmento; mentre l'altra configurazione aggrega un oggetto impostazione della scheda di rete diverso, specifico di un altro segmento. Si noti che molte impostazioni del computer sono indipendenti dalla configurazione di rete. Ad esempio, entrambe le configurazioni aggregano lo stesso oggetto impostazione per la risoluzione del monitor del computer.

> [!IMPORTANT]
> Le classi CIM (Distributed Management Task Force) DMTF (Distributed Management Task Force) Common Information Model sono le classi padre su cui vengono compilate le classi WMI. WMI supporta attualmente solo gli [schemi della versione CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal Managed Object Format (MOF) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

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

La **classe \_ CIM SettingContext** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe CIM \_ SettingContext** ha queste proprietà.

<dl> <dt>

**Contesto**
</dt> <dd> <dl> <dt>

Tipo di dati: **Configurazione \_ CIM**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Riferimento all'oggetto di configurazione che aggrega l'impostazione.

</dd> <dt>

**Impostazione**
</dt> <dd> <dl> <dt>

Tipo di dati: **Impostazione \_ CIM**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Riferimento a un'impostazione aggregata.

</dd> </dl>

## <a name="remarks"></a>Commenti

WMI non implementa questa classe.

Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF. Microsoft potrebbe aver apportato modifiche per correggere errori secondari, essere conforme agli standard della documentazione di Microsoft SDK o fornire altre informazioni.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

