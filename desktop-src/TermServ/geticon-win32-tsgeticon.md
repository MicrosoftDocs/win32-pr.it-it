---
title: Metodo GetIcon della classe Win32_TSGetIcon
description: Restituisce il contenuto dell'icona specificata.
ms.assetid: 9448181c-27b8-40eb-9369-8abe1422243b
ms.tgt_platform: multiple
keywords:
- Metodo GetIcon Servizi Desktop remoto
- Metodo GetIcon Servizi Desktop remoto, classe Win32_TSGetIcon
- Classe Win32_TSGetIcon Servizi Desktop remoto, Metodo GetIcon
topic_type:
- apiref
api_name:
- Win32_TSGetIcon.GetIcon
api_location:
- TsPubWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92cd20cad668b0e3a6bba191c83ecdca2934ca17
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963847"
---
# <a name="geticon-method-of-the-win32_tsgeticon-class"></a>Metodo GetIcon della classe Win32 \_ TSGetIcon

Restituisce il contenuto dell'icona specificata.

## <a name="syntax"></a>Sintassi


```mof
uint32 GetIcon(
  [in]  string FilePath,
  [in]  sint32 Index,
  [out] uint8  IconContents[]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*FilePath* \[ in\]
</dt> <dd>

Specifica il percorso del file che contiene l'icona.

</dd> <dt>

*Indice* \[ di in\]
</dt> <dd>

Specifica l'indice dell'icona nel file.

</dd> <dt>

*IconContents* \[ out\]
</dt> <dd>

Al termine, contiene il contenuto dell'icona.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                          |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TsAllow. mof</dt> </dl>  |
| DLL<br/>                      | <dl> <dt>TsPubWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_TSGetIcon Win32**](win32-tsgeticon.md)
</dt> </dl>

 

 





