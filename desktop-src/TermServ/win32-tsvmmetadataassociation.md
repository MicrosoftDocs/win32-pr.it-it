---
title: Classe Win32_TSVmMetadataAssociation
description: Rappresenta un'associazione tra una macchina virtuale Desktop remoto e le relative proprietà dei metadati.
ms.assetid: 374b1a29-78de-45fd-97b3-c5a5b724e66b
ms.tgt_platform: multiple
keywords:
- Classe Win32_TSVmMetadataAssociation Servizi Desktop remoto
- Classe Win32_TSVmMetadataAssociation Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_TSVmMetadataAssociation
- Win32_TSVmMetadataAssociation.TSVm
- Win32_TSVmMetadataAssociation.MetadataItem
api_location:
- TSVmHostWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db3a68c20553eaf52903471d19df9df169ecde21
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301051"
---
# <a name="win32_tsvmmetadataassociation-class"></a>Win32 \_ TSVmMetadataAssociation (classe)

Rappresenta un'associazione tra una macchina virtuale Desktop remoto e le relative proprietà dei metadati.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[dynamic, Association, provider("Win32_TSVmHost_Prov"), AMENDMENT]
class Win32_TSVmMetadataAssociation
{
  Win32_TSVm             REF TSVm;
  Win32_TSVmMetadataItem REF MetadataItem;
};
```

## <a name="members"></a>Members

La classe **Win32 \_ TSVmMetadataAssociation** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **Win32 \_ TSVmMetadataAssociation** dispone di queste proprietà.

<dl> <dt>

**MetadataItem**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **Win32 \_ TSVmMetadataItem**](win32-tsvmmetadataitem.md)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Istanza della classe [**Win32 \_ TSVmMetadataItem**](win32-tsvmmetadataitem.md) che rappresenta i metadati per la macchina virtuale.

</dd> <dt>

**TSVm**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **Win32 \_ TSVm**](win32-tsvm.md)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Istanza della classe [**Win32 \_ TSVm**](win32-tsvm.md) che rappresenta la macchina virtuale.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                  |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                             |
| Spazio dei nomi<br/>                | Radice \\ CIMV2 \\ TerminalServices<br/>                                                   |
| MOF<br/>                      | <dl> <dt>TSVmHost. mof</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>TSVmHostWmi.dll</dt> </dl> |



 

