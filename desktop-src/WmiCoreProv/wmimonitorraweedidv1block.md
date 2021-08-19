---
description: Rappresenta i dati non elaborati da una struttura E-EDID (Enhanced Extended Display Identification Data) di Video Electronics Standard Association (VESA).
ms.assetid: a51b73bb-a5f7-4e01-9c88-780105e9952b
title: Classe WmiMonitorRawEEdidV1Block
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorRawEEdidV1Block
- WmiMonitorRawEEdidV1Block.Active
- WmiMonitorRawEEdidV1Block.InstanceName
- WmiMonitorRawEEdidV1Block.Id
- WmiMonitorRawEEdidV1Block.Type
- WmiMonitorRawEEdidV1Block.Content
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 72b82f2c6eb967f39823d5b56174bb82e7503ee56f676ffb49b65822ec435936
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118821146"
---
# <a name="wmimonitorraweedidv1block-class"></a>Classe WmiMonitorRawEEdidV1Block

La **classe WMI WmiMonitorRawEEdidV1Block** rappresenta i dati non elaborati da una struttura VESA (Video Electronics Standard Association) Enhanced Extended Display Identification Data (E-EDID). Questa struttura di dati a 128 byte contiene informazioni che descrivono la configurazione ottimale per una visualizzazione.

## <a name="syntax"></a>Sintassi

``` syntax
class WmiMonitorRawEEdidV1Block : MSMonitorClass
{
  boolean Active;
  string  InstanceName;
  uint8   Id;
  uint8   Type;
  uint8   Content[];
};
```

## <a name="members"></a>Members

La **classe WmiMonitorRawEEdidV1Block** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe WmiMonitorRawEEdidV1Block** ha queste proprietà.

<dl> <dt>

**Attivo**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica il monitoraggio attivo.

</dd> <dt>

**Contenuto**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Matrice di 128 byte che contiene il contenuto del blocco non elaborato.

</dd> <dt>

**Id**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Identità del blocco di dati.

</dd> <dt>

**InstanceName**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **chiave**
</dt> </dl>

Nome dell'istanza del monitoraggio specifica.

</dd> <dt>

**Tipo**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tipo di blocco dati. Nella tabella seguente sono elencati i possibili valori che possono essere restituiti.



| Valore                                                                                 | Significato                    |
|---------------------------------------------------------------------------------------|----------------------------|
| <dl> <dt>0 (0x0)</dt> </dl>    | Inizializzazione annullata<br/>   |
| <dl> <dt>1 (0x1)</dt> </dl>    | Blocco di base EDID<br/> |
| <dl> <dt>2 (0x2)</dt> </dl>    | Mappa a blocchi EDID<br/>  |
| <dl> <dt>255 (0xFF)</dt> </dl> | Altro<br/>           |



 

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                         |
| Spazio dei nomi<br/>                | Wmi \\ radice<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WmiCore.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MSMonitorClass**](msmonitorclass.md)
</dt> <dt>

[**WmiGetMonitorRawEEdidV1Block**](wmigetmonitorraweedidv1block-wmimonitordescriptormethods.md)
</dt> </dl>

 

 




