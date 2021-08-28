---
description: Altre informazioni sull'enumerazione StopServiceGrbit
title: Enumerazione StopServiceGrbit (Microsoft.Isam.Esent.Interop.Windows8)
TOCTitle: StopServiceGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.stopservicegrbit(v=EXCHG.10)
ms:contentKeyID: 55104330
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.All
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.BackgroundUserTasks
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.QuiesceCaches
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.Resume
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.BackgroundUserTasks
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.All
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.QuiesceCaches
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.Resume
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6c8280bf4abfbc9eb5818d1aab460a17298db7b0
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477457"
---
# <a name="stopservicegrbit-enumeration"></a>Enumerazione StopServiceGrbit

Opzioni per [JetStopServiceInstance2(JET_INSTANCE, StopServiceGrbit)](./windows8api.jetstopserviceinstance2-method.md).

Questa enumerazione ha un attributo [FlagsAttribute](/dotnet/api/system.flagsattribute) che consente una combinazione bit per bit dei valori del relativo membro.

**Spazio dei**  [nomi: Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration StopServiceGrbit
'Usage
Dim instance As StopServiceGrbit
```

``` csharp
[FlagsAttribute]
public enum StopServiceGrbit
```

## <a name="members"></a>Members


|  | Nome del membro | Descrizione | 
|--|-------------|-------------|
|  | Tutti | Arresta tutti i servizi ESE per l'istanza specificata. | 
|  | BackgroundUserTasks | Arresta le attività di manutenzione in background specifiche del client riavviabili (deframmentazione albero B+). | 
|  | QuiesceCaches | Inattiva tutte le cache dirty su disco. Asincrona. La disattivazione viene annullata se il bit Resume viene chiamato successivamente. | 
|  | Riprendi | Riprende le operazioni StopService eseguite in precedenza, ad esempio "riavvia il servizio". Può essere combinato con i grbit precedenti per riprendere servizi specifici o con 0x0 riprende tutti i servizi arrestati in precedenza.<p>Avviso: questo bit può essere usato solo per riprendere JET_bitStopServiceBackground e JET_bitStopServiceQuiesceCaches, se è stato eseguito un JET_bitStopServiceAll o un JET_bitStopServiceAPI, il tentativo di usare JET_bitStopServiceResume avrà esito negativo.</p> | 



## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Spazio dei nomi Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)
