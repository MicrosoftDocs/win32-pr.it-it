---
description: Questa classe è la classe del tipo di evento per gli eventi di fine dell'operazione su file. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 3925d5bf-f412-4248-a61f-e667efa9debd
title: Classe FileIo_OpEnd
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_OpEnd
- FileIo_OpEnd.IrpPtr
- FileIo_OpEnd.ExtraInfo
- FileIo_OpEnd.NtStatus
api_type:
- NA
api_location: ''
ms.openlocfilehash: d3f1c495cf44b84f8d7661b40cadec6ea255c6a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758429"
---
# <a name="fileio_opend-class"></a>\_Classe aprita FileIO

Questa classe è la classe del tipo di evento per gli eventi di fine dell'operazione su file.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[EventType{76}, EventTypeName{"OperationEnd"}]
class FileIo_OpEnd : FileIo
{
  uint32 IrpPtr;
  uint32 ExtraInfo;
  uint32 NtStatus;
};
```

## <a name="members"></a>Members

I tipi di membri della classe **\_ Open FileIO** sono i seguenti:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

Le proprietà della classe **\_ Aprita del FileIO** sono tali.

<dl> <dt>

**ExtraInfo**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (2), puntatore
</dt> </dl>

Informazioni aggiuntive restituite dal file system per l'operazione. Ad esempio, per una richiesta di lettura, il numero effettivo di byte letti.

</dd> <dt>

**IrpPtr**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (1), puntatore
</dt> </dl>

Pacchetto di richiesta IO. Questa proprietà identifica l'attività IO che sta terminando.

</dd> <dt>

**NtStatus**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (3)
</dt> </dl>

Valore restituito dall'operazione.

</dd> </dl>

## <a name="remarks"></a>Commenti

Gli eventi [**FileIO**](fileio.md) vengono registrati all'inizio dell'operazione. Gli eventi aperti possono essere abilitati separatamente per indicare la fine di tali operazioni. È possibile utilizzare l'IRP per correlare gli eventi di inizio e di fine.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**FileIo**](fileio.md)
</dt> </dl>

 

 




