---
title: Messaggio di ICM_DECOMPRESSEX_BEGIN (VFW. h)
description: Il \_ messaggio Begin DECOMPRESSEX di ICM \_ notifica a un driver di compressione video di preparare la decompressione dei dati.
ms.assetid: 35298274-91b5-4df0-b4b0-4a71d6a49990
keywords:
- ICM_DECOMPRESSEX_BEGIN messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- ICM_DECOMPRESSEX_BEGIN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77ea082c91d48a9964348b762ce13631cd80af30
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742954"
---
# <a name="icm_decompressex_begin-message"></a>\_Messaggio di \_ inizio DECOMPRESSEX ICM

Il **messaggio \_ \_ Begin DECOMPRESSEX di ICM** notifica a un driver di compressione video di preparare la decompressione dei dati.


```C++
ICM_DECOMPRESSEX_BEGIN 
wParam = (DWORD_PTR) (LPVOID) &icdex; 
lParam = sizeof(ICDECOMPRESSEX); 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="icdex"></span><span id="ICDEX"></span>*icdex*
</dt> <dd>

Puntatore a una struttura [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex) contenente i formati di input e di output.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Dimensioni, in byte, di [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce ICERR \_ OK se la decompressione specificata è supportata o ICERR \_ BADFORMAT in caso contrario.

## <a name="remarks"></a>Commenti

Quando il driver riceve questo messaggio, deve allocare buffer ed eseguire operazioni che richiedono molto tempo, in modo che sia in grado di elaborare i messaggi [**\_ DECOMPRESSEX ICM**](icm-decompressex.md) in modo efficiente.

Se si vuole che il driver decomprimere i dati direttamente sullo schermo, inviare il messaggio di [**\_ \_ inizio del progetto ICM**](icm-draw-begin.md) .

I **messaggi \_ DECOMPRESSEX \_ Begin** e [**ICM \_ DECOMPRESSEX \_ end**](icm-decompressex-end.md) non vengono annidati. Se il driver riceve **la \_ DECOMPRESSEX MCI \_ iniziare** prima che la decompressione venga interrotta con la **\_ \_ fine di DECOMPRESSEX ICM**, dovrebbe riavviare la decompressione con nuovi parametri.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Gestione compressione video](video-compression-manager.md)
</dt> <dt>

[Messaggi di compressione video](video-compression-messages.md)
</dt> </dl>

 

 





