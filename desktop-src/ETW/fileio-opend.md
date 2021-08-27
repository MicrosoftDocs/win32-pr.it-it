---
description: Questa classe è la classe del tipo di evento per gli eventi di fine dell'operazione su file. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 3925d5bf-f412-4248-a61f-e667efa9debd
title: FileIo_OpEnd classe
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
ms.openlocfilehash: 74042df74f8e128c4d92b6e4f1c886a7bba2f673c1a8a998a4b7f251475c3f93
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130591"
---
# <a name="fileio_opend-class"></a>Classe FileIo \_ OpEnd

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

La **classe FileIo \_ OpEnd** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe FileIo \_ OpEnd** ha queste proprietà.

<dl> <dt>

**ExtraInfo**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(2), Puntatore
</dt> </dl>

Informazioni aggiuntive restituite dal file system per l'operazione. Ad esempio, per una richiesta di lettura, il numero effettivo di byte letti.

</dd> <dt>

**IrpPtr**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(1), Pointer
</dt> </dl>

Pacchetto di richiesta I/O. Questa proprietà identifica l'attività di I/O che termina.

</dd> <dt>

**NtStatus**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(3)
</dt> </dl>

Valore restituito dall'operazione.

</dd> </dl>

## <a name="remarks"></a>Commenti

[**Gli eventi FileIo**](fileio.md) vengono registrati all'inizio dell'operazione. Gli eventi OpEnd possono essere abilitati separatamente per indicare la fine di tali operazioni. Irp può essere usato per correlare gli eventi di inizio e fine.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Fileio**](fileio.md)
</dt> </dl>

 

 




