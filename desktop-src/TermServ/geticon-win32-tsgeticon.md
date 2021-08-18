---
title: Metodo GetIcon della Win32_TSGetIcon classe
description: Restituisce il contenuto dell'icona specificata.
ms.assetid: 9448181c-27b8-40eb-9369-8abe1422243b
ms.tgt_platform: multiple
keywords:
- Metodo GetIcon Servizi Desktop remoto
- Metodo GetIcon Servizi Desktop remoto , Win32_TSGetIcon classe
- Win32_TSGetIcon classe Servizi Desktop remoto , metodo GetIcon
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
ms.openlocfilehash: 305316d66ce95659210396a10f22366d64ebdd2b410b056aa3c398cf65edbbf5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001539"
---
# <a name="geticon-method-of-the-win32_tsgeticon-class"></a>Metodo GetIcon della classe \_ Win32 TSGetIcon

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

*FilePath* \[ Pollici\]
</dt> <dd>

Specifica il percorso del file che contiene l'icona

</dd> <dt>

*Indice* \[ Pollici\]
</dt> <dd>

Specifica l'indice dell'icona nel file.

</dd> <dt>

*IconContents* \[ Cambio\]
</dt> <dd>

Al completamento, contiene il contenuto dell'icona.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                          |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TsAllow.mof</dt> </dl>  |
| DLL<br/>                      | <dl> <dt>TsPubWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ TSGetIcon**](win32-tsgeticon.md)
</dt> </dl>

 

 





