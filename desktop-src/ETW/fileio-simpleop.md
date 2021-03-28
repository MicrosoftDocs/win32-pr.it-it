---
description: Questa classe è la classe del tipo di evento per gli eventi semplici dell'operazione sui file. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 5b6374e0-b39a-4d5a-acbd-25b410f1ba52
title: Classe FileIo_SimpleOp
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_SimpleOp
- FileIo_SimpleOp.IrpPtr
- FileIo_SimpleOp.TTID
- FileIo_SimpleOp.FileObject
- FileIo_SimpleOp.FileKey
api_type:
- NA
api_location: ''
ms.openlocfilehash: f7ff09830653278c9b37cfefa81b182b0f1dc054
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980362"
---
# <a name="fileio_simpleop-class"></a>Classe SimpleOp di FileIO \_

Questa classe è la classe del tipo di evento per gli eventi semplici dell'operazione sui file.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[EventType{65, 66, 73}, EventTypeName{"Cleanup", "Close", "Flush"}]
class FileIo_SimpleOp : FileIo
{
  uint32 IrpPtr;
  uint32 TTID;
  uint32 FileObject;
  uint32 FileKey;
};
```

## <a name="members"></a>Members

La **classe \_ SimpleOp di FileIO** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ SimpleOp di FileIO** presenta queste proprietà.

<dl> <dt>

**FileKey**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (4), puntatore
</dt> </dl>

Per determinare il nome del file, trovare la corrispondenza con il valore di questa proprietà con la proprietà **FileObject** di un evento del [**\_ nome**](fileio-name.md) del FileIO.

</dd> <dt>

**FileObject**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (3), puntatore
</dt> </dl>

Identificatore che può essere usato per correlare le operazioni alla stessa istanza dell'oggetto file aperto tra gli eventi di creazione e chiusura di file.

</dd> <dt>

**IrpPtr**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (1), puntatore
</dt> </dl>

Pacchetto di richiesta IO. Questa proprietà identifica l'attività IO.

</dd> <dt>

**TTID**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (2), puntatore
</dt> </dl>

Identificatore del thread che sta eseguendo l'operazione.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'evento Cleanup viene registrato quando viene chiuso l'ultimo handle del file. L'evento Close specifica che un oggetto file viene liberato. L'evento Flush specifica quando i buffer di file vengono scaricati completamente su disco.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**FileIo**](fileio.md)
</dt> </dl>

 

 




