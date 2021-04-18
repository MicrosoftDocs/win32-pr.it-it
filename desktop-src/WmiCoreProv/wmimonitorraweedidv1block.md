---
description: Rappresenta i dati non elaborati di una struttura EDID (video Electronics Standard Association) migliorata.
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
ms.openlocfilehash: 79566dccceb36281c9b3a94b19fed2ed5679dc8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313690"
---
# <a name="wmimonitorraweedidv1block-class"></a>Classe WmiMonitorRawEEdidV1Block

La classe WMI **WmiMonitorRawEEdidV1Block** rappresenta i dati non elaborati da una struttura di EDID (video Electronics Standard Association) migliorata. Questa struttura di dati a 128 byte contiene informazioni che descrivono la configurazione ottimale per una visualizzazione.

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

La classe **WmiMonitorRawEEdidV1Block** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **WmiMonitorRawEEdidV1Block** dispone di queste proprietà.

<dl> <dt>

**Attivo**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica il monitoraggio attivo.

</dd> <dt>

**Contenuto**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **Uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

matrice di byte 128 che contiene il contenuto del blocco non elaborato.

</dd> <dt>

**Id**
</dt> <dd> <dl> <dt>

Tipo di dati: **Uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Identità del blocco di dati.

</dd> <dt>

**InstanceName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **chiave**
</dt> </dl>

Nome dell'istanza di monitoraggio specifica.

</dd> <dt>

**Tipo**
</dt> <dd> <dl> <dt>

Tipo di dati: **Uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tipo di blocco di dati. Nella tabella seguente sono elencati i valori possibili che possono essere restituiti.



| Valore                                                                                 | Significato                    |
|---------------------------------------------------------------------------------------|----------------------------|
| <dl> <dt>0 (0x0)</dt> </dl>    | Inizializzazione annullata<br/>   |
| <dl> <dt>1 (0x1)</dt> </dl>    | Blocco base EDID<br/> |
| <dl> <dt>2 (0x2)</dt> </dl>    | Mappa di blocco EDID<br/>  |
| <dl> <dt>255 (0xFF)</dt> </dl> | Altro<br/>           |



 

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                         |
| Spazio dei nomi<br/>                | \\WMI radice<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WmiCore. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MSMonitorClass**](msmonitorclass.md)
</dt> <dt>

[**WmiGetMonitorRawEEdidV1Block**](wmigetmonitorraweedidv1block-wmimonitordescriptormethods.md)
</dt> </dl>

 

 




