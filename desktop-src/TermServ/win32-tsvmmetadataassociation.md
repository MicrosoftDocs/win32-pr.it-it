---
title: Win32_TSVmMetadataAssociation classe
description: Rappresenta un'associazione tra una Desktop remoto virtuale e le relative proprietà dei metadati.
ms.assetid: 374b1a29-78de-45fd-97b3-c5a5b724e66b
ms.tgt_platform: multiple
keywords:
- Win32_TSVmMetadataAssociation classe Servizi Desktop remoto
- Win32_TSVmMetadataAssociation classe Servizi Desktop remoto , descritto
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
ms.openlocfilehash: ebe3389bb03c9e3f33a2cc3e33450318b68171f7ac35fffeaaa3976cb5ae3a33
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119420001"
---
# <a name="win32_tsvmmetadataassociation-class"></a>Classe \_ Win32 TSVmMetadataAssociation

Rappresenta un'associazione tra una Desktop remoto virtuale e le relative proprietà dei metadati.

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

La **classe \_ Win32 TSVmMetadataAssociation** include questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ Win32 TSVmMetadataAssociation** ha queste proprietà.

<dl> <dt>

**MetadataItem**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **Win32 \_ TSVmMetadataItem**](win32-tsvmmetadataitem.md)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Istanza della classe [**\_ Win32 TSVmMetadataItem**](win32-tsvmmetadataitem.md) che rappresenta i metadati per la macchina virtuale.

</dd> <dt>

**TSVm**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **\_ TSVm Win32**](win32-tsvm.md)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Istanza della classe [**\_ TSVm Win32**](win32-tsvm.md) che rappresenta la macchina virtuale.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                  |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                             |
| Spazio dei nomi<br/>                | Radice \\ CIMV2 \\ TerminalServices<br/>                                                   |
| MOF<br/>                      | <dl> <dt>TSVmHost.mof</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>TSVmHostWmi.dll</dt> </dl> |



 

