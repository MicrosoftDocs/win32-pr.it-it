---
title: Proprietà SystemMonitor. GraphTitle
description: Recupera o imposta il titolo del grafico.
ms.assetid: 10a91b38-6963-4ef6-8b4f-9ecd1341f471
keywords:
- Proprietà GraphTitle SysMon
- Proprietà GraphTitle SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon, proprietà GraphTitle
topic_type:
- apiref
api_name:
- SystemMonitor.GraphTitle
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55918b67eb88b8c2c1aca99ce6e86f190ad1a395
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517794"
---
# <a name="systemmonitorgraphtitle-property"></a>Proprietà SystemMonitor. GraphTitle

Recupera o imposta il titolo del grafico.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```VB
Property GraphTitle As String
```



## <a name="property-value"></a>Valore proprietà

Titolo del grafico. La lunghezza massima del titolo è di 128 caratteri. Se il titolo supera i 128 caratteri, il titolo viene troncato.

**Windows XP e windows 2000:** Non esiste alcun limite alla lunghezza del titolo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                            |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> </dl>

 

 





