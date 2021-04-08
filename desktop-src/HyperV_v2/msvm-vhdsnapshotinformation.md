---
description: Fornisce informazioni su uno snapshot in un file di set VHD.
ms.assetid: 922bf0b8-523d-488e-9a41-1a27594e2e44
title: Classe Msvm_VHDSnapshotInformation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VHDSnapshotInformation
- Msvm_VHDSnapshotInformation.FilePath
- Msvm_VHDSnapshotInformation.SnapshotId
- Msvm_VHDSnapshotInformation.SnapshotPath
- Msvm_VHDSnapshotInformation.ParentPathsList
- Msvm_VHDSnapshotInformation.CreationTime
- Msvm_VHDSnapshotInformation.ResilientChangeTrackingId
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1a1e2a573546d62d79170f15abddd8d5c17e30f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879930"
---
# <a name="msvm_vhdsnapshotinformation-class"></a>\_Classe MSVM VHDSnapshotInformation

Fornisce informazioni su uno snapshot in un file di set VHD

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[AMENDMENT]
class Msvm_VHDSnapshotInformation
{
  string   FilePath;
  string   SnapshotId;
  string   SnapshotPath;
  string   ParentPathsList[];
  DATETIME CreationTime;
  string   ResilientChangeTrackingId;
};
```

## <a name="members"></a>Members

La **classe \_ VHDSnapshotInformation di MSVM** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ VHDSnapshotInformation di MSVM** dispone di queste proprietà.

<dl> <dt>

**CreationTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Data e ora della creazione dello snapshot.

</dd> <dt>

**FilePath**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Percorso del file di set VHD.

</dd> <dt>

**ParentPathsList**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Elenco di percorsi di file che rappresentano tutti i file da cui dipende questo snapshot. Questo campo sarà vuoto a meno che non sia richiesto in modo specifico. La prima voce è l'elemento padre diretto del file, con l'ultima voce che corrisponde alla radice.

</dd> <dt>

**ResilientChangeTrackingId**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

ID di rilevamento delle modifiche resiliente, se presente, associato a questo snapshot.

</dd> <dt>

**SnapshotId**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

GUID che identifica in modo univoco questo snapshot all'interno del file di set VHD.

</dd> <dt>

**SnapshotPath**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Percorso del file rappresentato da questo snapshot. Questo campo può essere vuoto se non è presente alcun file associato a questo snapshot.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows 10\]<br/>                                                             |
| Server minimo supportato<br/> | Windows Server 2016<br/>                                                                          |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

 




