---
description: Fornisce informazioni su un file di set di dischi rigidi virtuali.
ms.assetid: a975c131-d3f3-4be3-bc69-e277e3ce4d28
title: Msvm_VHDSetInformation classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VHDSetInformation
- Msvm_VHDSetInformation.Path
- Msvm_VHDSetInformation.SnapshotIdList
- Msvm_VHDSetInformation.AllPaths
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d8cef737c02629ac0a1a026a459adf6eb7060e0dbdf8c0f9ecb20c66fce1259e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119789431"
---
# <a name="msvm_vhdsetinformation-class"></a>Classe Msvm \_ VHDSetInformation

Fornisce informazioni su un file di set di dischi rigidi virtuali.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[AMENDMENT]
class Msvm_VHDSetInformation
{
  string Path;
  string SnapshotIdList[];
  string AllPaths[];
};
```

## <a name="members"></a>Members

La **classe Msvm \_ VHDSetInformation** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Msvm \_ VHDSetInformation** ha queste proprietà.

<dl> <dt>

**AllPaths**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Elenco di tutti i file inclusi nel file del set di dischi rigidi virtuali, inclusi tutti i file senza riferimenti e tutti gli elementi padre del disco rigido virtuale radice. Tutti i file elencati dopo il disco rigido virtuale radice non vengono gestiti da questo file del set di dischi rigidi virtuali. Questo campo può essere vuoto se queste informazioni non sono richieste in modo specifico.

</dd> <dt>

**Percorso**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Percorso del file del set di dischi rigidi virtuali.

</dd> <dt>

**SnapshotIdList**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Elenco di GUID che rappresentano tutti gli snapshot contenuti in questo file di set di dischi rigidi virtuali.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                                             |
| Server minimo supportato<br/> | Windows Server 2016<br/>                                                                          |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

 




