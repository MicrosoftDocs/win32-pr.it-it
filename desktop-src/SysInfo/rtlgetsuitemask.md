---
description: Recupera una maschera di bit che identifica i gruppi di prodotti disponibili nel sistema. Se questa funzione viene chiamata in un'applicazione che viene eseguita nel contesto di un silo di server, viene invece recuperata la maschera di gruppo per il silo del server.
ms.assetid: 1D6434FD-D7BD-45F9-B7C3-238890AF9928
title: Funzione RtlGetSuiteMask (ntddk. h)
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
ms.openlocfilehash: ed8d8906273d18125131251636bc6199d166547b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315298"
---
# <a name="rtlgetsuitemask-function"></a>RtlGetSuiteMask (funzione)

\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

Recupera una maschera di bit che identifica i gruppi di prodotti disponibili nel sistema. Se questa funzione viene chiamata in un'applicazione che viene eseguita nel contesto di un silo di server, viene invece recuperata la maschera di gruppo per il silo del server.

## <a name="syntax"></a>Sintassi


```C++
ULONG NTAPI RtlGetSuiteMask(void);
```



## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

Maschera di bit che identifica i gruppi di prodotti disponibili nel sistema. La maschera di bit può includere i valori seguenti.



| Valore restituito                                                                          | Descrizione                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0x00000001</dt> </dl> | Microsoft Small Business Server è stato installato nel sistema, ma potrebbe essere stato aggiornato a un'altra versione di Windows. Per ulteriori informazioni su questo flag di bit, vedere la sezione Osservazioni.<br/>                                           |
| <dl> <dt>0x00000002</dt> </dl> | Windows 10 Enterprise, Windows 8.1 Enterprise, Windows Server 2008 Enterprise, Windows Server 2003, Enterprise Edition o Windows 2000 Advanced Server è installato. Per ulteriori informazioni su questo flag di bit, vedere la sezione Osservazioni.<br/> |
| <dl> <dt>0x00000004</dt> </dl> | Microsoft BackOffice Components è installato.<br/>                                                                                                                                                                                               |
| <dl> <dt>0x00000008</dt> </dl> | Communications Server 2003, Communications Server 2005, Communications Server 2007 o Communications Server 2007 R2 è installato.<br/>                                                                                                           |
| <dl> <dt>0x00000010</dt> </dl> | Servizi terminal è installato. Questo valore è sempre impostato.<br/> Se **TerminalServer** è impostato ma **SingleUserTS** non è impostato, il sistema viene eseguito in modalità server applicazioni.<br/>                                                         |
| <dl> <dt>0x00000020</dt> </dl> | Microsoft Small Business Server viene installato con la licenza client restrittiva in vigore. Per ulteriori informazioni su questo flag di bit, vedere la sezione Osservazioni.<br/>                                                                            |
| <dl> <dt>0x00000040</dt> </dl> | Windows XP Embedded è installato.<br/>                                                                                                                                                                                                            |
| <dl> <dt>0x00000080</dt> </dl> | Windows Server 2008 Datacenter, Windows Server 2003, Datacenter Edition o Windows 2000 Datacenter Server è installato.<br/>                                                                                                                     |
| <dl> <dt>0x00000100</dt> </dl> | Desktop remoto è supportato, ma è supportata una sola sessione interattiva. Questo valore viene impostato a meno che il sistema non sia in esecuzione in modalità server applicazioni.<br/>                                                                                       |
| <dl> <dt>0x00000200</dt> </dl> | Windows Vista Home Premium, Windows Vista Home Basic o Windows XP Home Edition è installato.<br/>                                                                                                                                               |
| <dl> <dt>0x00000400</dt> </dl> | Windows Server 2003, Web Edition è installato.<br/>                                                                                                                                                                                               |
| <dl> <dt>0x00002000</dt> </dl> | Windows Storage Server 2003 R2 o Windows Storage Server 2003 è installato.<br/>                                                                                                                                                                  |
| <dl> <dt>0x00004000</dt> </dl> | Windows Server 2003, Compute Cluster Edition è installato.<br/>                                                                                                                                                                                   |
| <dl> <dt>0x00008000</dt> </dl> | Windows Home Server è installato.<br/>                                                                                                                                                                                                            |



 

## <a name="remarks"></a>Commenti

Si consiglia di non basarsi solo sul flag 0x00000001 per determinare se Small Business Server è stato installato nel sistema, poiché sia questo flag che il flag 0x00000020 vengono impostati quando viene installato questo gruppo di prodotti. Se si aggiorna questa installazione a Windows Server, Standard Edition, il flag 0x00000020 verrà cancellato, tuttavia, il flag 0x00000001 rimarrà impostato. In questo caso, significa che Small Business Server è stato installato in questo sistema. Se questa installazione viene aggiornata ulteriormente a Windows Server, Enterprise Edition, il flag 0x00000001 rimarrà impostato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows 10\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2016\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Ntddk. h</dt> </dl>   |
| Libreria<br/>                  | <dl> <dt>Ntdll. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 




