---
title: MDM_Reboot classe
description: La classe Reboot di MDM \_ viene usata per configurare le impostazioni di riavvio.
ms.assetid: 876ba854-1c26-49cf-915d-194be9f9c1d4
keywords:
- MDM_Reboot classe
- MDM_Reboot classe , descritta
topic_type:
- apiref
api_name:
- MDM_Reboot
- MDM_Reboot.InstanceID
- MDM_Reboot.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b742754cc22d069cce47ef32a60739c517f578df76fc42dbf5076972c5e63b0c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119967491"
---
# <a name="mdm_reboot-class"></a>Classe \_ reboot MDM

\[Alcune informazioni riguardano un prodotto pre-rilasciato che può essere modificato sostanzialmente prima del rilascio in commercio. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

La **classe \_ Reboot MDM** viene usata per configurare le impostazioni di riavvio.

La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Reboot
{
  string InstanceID;
  string ParentID;
};
```

## <a name="members"></a>Members

La **classe \_ Reboot MDM** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe \_ Reboot MDM** dispone di questi metodi.



| Metodo                                                | Descrizione                                             |
|:------------------------------------------------------|:--------------------------------------------------------|
| [**RebootNowMethod**](mdm-reboot-rebootnowmethod.md) | Questo metodo esegue un riavvio del dispositivo.<br/> |



 

### <a name="properties"></a>Proprietà

La **classe \_ Reboot MDM** ha queste proprietà.

<dl> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identifica il nome del nodo padre. Per questa classe, la stringa è "Reboot".

</dd> <dt>

**Parentid**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Descrive il percorso completo del nodo padre. Per questa classe, la stringa è "./Vendor/MSFT/"

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                                          |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                            |
| Spazio dei nomi<br/>                | Dmmap \\ mdm cimv2 \\ \\ radice<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv1.mof</dt> </dl>      |
| DLL<br/>                      | <dl> <dt>File mofs \\DMWmiBridgeProv.dll</dt> </dl> |



 

