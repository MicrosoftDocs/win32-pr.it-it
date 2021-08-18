---
description: Recupera una maschera di bit che identifica le suite di prodotti disponibili nel sistema. Se questa funzione viene chiamata in un'applicazione eseguita nel contesto di un silo del server, viene recuperata la maschera della suite per il silo del server.
ms.assetid: 1D6434FD-D7BD-45F9-B7C3-238890AF9928
title: Funzione RtlGetSuiteMask (Ntddk.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlGetSuiteMask
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: c6a71a2cb697021edcf8cea3da8759bbe40aa8ed9be2a93f8adcbeba4197ef88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117763470"
---
# <a name="rtlgetsuitemask-function"></a>Funzione RtlGetSuiteMask

\[Alcune informazioni riguardano un prodotto pre-rilasciato che può essere modificato sostanzialmente prima del rilascio in commercio. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

Recupera una maschera di bit che identifica le suite di prodotti disponibili nel sistema. Se questa funzione viene chiamata in un'applicazione eseguita nel contesto di un silo del server, viene recuperata la maschera della suite per il silo del server.

## <a name="syntax"></a>Sintassi


```C++
ULONG NTAPI RtlGetSuiteMask(void);
```



## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

Maschera di bit che identifica le suite di prodotti disponibili nel sistema. La maschera di bit può includere i valori seguenti.



| Valore restituito                                                                          | Descrizione                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0x00000001</dt> </dl> | Microsoft Small Business Server è stato installato nel sistema, ma potrebbe essere stato aggiornato a un'altra versione di Windows. Per altre informazioni su questo flag di bit, vedere la sezione Osservazioni.<br/>                                           |
| <dl> <dt>0x00000002</dt> </dl> | Windows 10 Enterprise, Windows 8.1 Enterprise, Windows Server 2008 Enterprise, Windows Server 2003, edizione Enterprise o Windows 2000 Advanced Server è installato. Per altre informazioni su questo flag di bit, vedere la sezione Osservazioni.<br/> |
| <dl> <dt>0x00000004</dt> </dl> | Vengono installati i componenti Microsoft BackOffice.<br/>                                                                                                                                                                                               |
| <dl> <dt>0x00000008</dt> </dl> | Communications Server 2003, Communications Server 2005, Communications Server 2007 o Communications Server 2007 R2 è installato.<br/>                                                                                                           |
| <dl> <dt>0x00000010</dt> </dl> | Servizi terminal è installato. Questo valore è sempre impostato.<br/> Se **TerminalServer è** impostato ma **SingleUserTS** non è impostato, il sistema è in esecuzione in modalità server applicazioni.<br/>                                                         |
| <dl> <dt>0x00000020</dt> </dl> | Microsoft Small Business Server viene installato con la licenza client restrittiva in vigore. Per altre informazioni su questo flag di bit, vedere la sezione Osservazioni.<br/>                                                                            |
| <dl> <dt>0x00000040</dt> </dl> | Windows XP Embedded è installato.<br/>                                                                                                                                                                                                            |
| <dl> <dt>0x00000080</dt> </dl> | Windows È installato Server 2008 Datacenter, Windows Server 2003, Datacenter Edition o Windows 2000 Datacenter Server.<br/>                                                                                                                     |
| <dl> <dt>0x00000100</dt> </dl> | Desktop remoto è supportato, ma è supportata una sola sessione interattiva. Questo valore viene impostato a meno che il sistema non sia in esecuzione in modalità server applicazioni.<br/>                                                                                       |
| <dl> <dt>0x00000200</dt> </dl> | Windows Vista Home Premium, Windows Vista Home Basic o Windows XP Home Edition è installato.<br/>                                                                                                                                               |
| <dl> <dt>0x00000400</dt> </dl> | Windows Server 2003, Web Edition è installato.<br/>                                                                                                                                                                                               |
| <dl> <dt>0x00002000</dt> </dl> | Windows Archiviazione Server 2003 R2 o Windows Archiviazione Server 2003.<br/>                                                                                                                                                                  |
| <dl> <dt>0x00004000</dt> </dl> | Windows Server 2003, Compute Cluster Edition è installato.<br/>                                                                                                                                                                                   |
| <dl> <dt>0x00008000</dt> </dl> | Windows Home Server è installato.<br/>                                                                                                                                                                                                            |



 

## <a name="remarks"></a>Commenti

È consigliabile non fare affidamento solo sul flag 0x00000001 per determinare se Small Business Server è stato installato nel sistema, perché sia questo flag che il flag 0x00000020 vengono impostati durante l'installazione di questa famiglia di prodotti. Se si aggiorna questa installazione a Windows Server, edizione Standard, il flag 0x00000020 verrà cancellato, ma il flag di 0x00000001 rimarrà impostato. In questo caso, indica che Small Business Server è stato installato in questo sistema. Se questa installazione viene ulteriormente aggiornata a Windows Server, edizione Enterprise, il flag 0x00000001 verrà impostato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                          |
| Server minimo supportato<br/> | \[Windows Server 2016 solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Ntddk.h</dt> </dl>   |
| Libreria<br/>                  | <dl> <dt>Ntdll.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 




