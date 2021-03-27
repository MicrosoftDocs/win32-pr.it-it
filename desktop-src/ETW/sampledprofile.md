---
description: Questa classe è la classe del tipo di evento per gli eventi del profilo campionati. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 75ea1e5e-2554-40bb-aa9d-c6d4942c5801
title: Classe SampledProfile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SampledProfile
- SampledProfile.InstructionPointer
- SampledProfile.ThreadId
- SampledProfile.Count
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3d7a69eef1a2a7988569ffcd930b73a559e18d90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980554"
---
# <a name="sampledprofile-class"></a>Classe SampledProfile

Questa classe è la classe del tipo di evento per gli eventi del profilo campionati.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[EventType{46}, EventTypeName{"SampleProfile"}]
class SampledProfile : PerfInfo
{
  uint32 InstructionPointer;
  uint32 ThreadId;
  uint32 Count;
};
```

## <a name="members"></a>Members

La classe **SampledProfile** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **SampledProfile** dispone di queste proprietà.

<dl> <dt>

**Count**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (3)
</dt> </dl>

Non usato.

</dd> <dt>

**InstructionPointer**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (1), puntatore
</dt> </dl>

Indirizzo dell'immagine in esecuzione al momento del campionamento del processore.

</dd> <dt>

**ThreadId**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (2)
</dt> </dl>

Identificatore del thread che era in esecuzione al momento del campionamento del processore.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questi eventi forniscono un profilo di esecuzione campionato. L'evento registra gli elementi eseguiti sul processore. È possibile usare gli eventi di immagine per identificare il modulo binario contenente tale istruzione. È quindi possibile usare queste informazioni per produrre un profilo di esecuzione per la durata della traccia.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 




