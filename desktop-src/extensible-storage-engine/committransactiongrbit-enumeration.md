---
description: Altre informazioni sull'enumerazione CommitTransactionGrbit
title: Enumerazione CommitTransactionGrbit
TOCTitle: CommitTransactionGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.CommitTransactionGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.committransactiongrbit(v=EXCHG.10)
ms:contentKeyID: 39510830
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit.None
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit.WaitLastLevel0Commit
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit.LazyFlush
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit.WaitLastLevel0Commit
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit.LazyFlush
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit
- Microsoft.Isam.Esent.Interop.CommitTransactionGrbit.None
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: efe052fc01014d3ebb624dbd4183bc8f0584b145
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481787"
---
# <a name="committransactiongrbit-enumeration"></a>Enumerazione CommitTransactionGrbit

Opzioni per JetCommitTransaction.

Questa enumerazione ha un attributo [FlagsAttribute](/dotnet/api/system.flagsattribute) che consente una combinazione bit per bit dei valori del relativo membro.

**Spazio dei**  [nomi: Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration CommitTransactionGrbit
'Usage
Dim instance As CommitTransactionGrbit
```

``` csharp
[FlagsAttribute]
public enum CommitTransactionGrbit
```

## <a name="members"></a>Members


|  | Nome del membro | Descrizione | 
|--|-------------|-------------|
|  | nessuno | Opzioni predefinite. | 
|  | LazyFlush | Il commit della transazione viene eseguito normalmente, ma questa API non attende che la transazione venga scaricata nel file di log delle transazioni prima di tornare al chiamante. In questo modo si riduce drasticamente la durata di un'operazione di commit a s costo della durabilità. Qualsiasi transazione che non viene scaricata nel log prima di un arresto anomalo del sistema verrà interrotta automaticamente durante il recupero dall'arresto anomalo del sistema durante la chiamata successiva a JetInit. Se si specifica WaitLastLevel0Commit o WaitAllLevel0Commit, questa opzione viene ignorata. | 
|  | WaitLastLevel0Commit | Se in precedenza la sessione ha eseguito il commit di transazioni e non sono ancora state scaricate nel file di log delle transazioni, devono essere scaricate immediatamente. Questa API attenderà che le transazioni siano state scaricate prima di tornare al chiamante. Ciò è utile se in precedenza l'applicazione ha eseguito il commit di più transazioni usando JET_bitCommitLazyFlush e ora vuole scaricarle tutte su disco.<p>Questa opzione può essere utilizzata anche se la sessione non è attualmente in una transazione. Questa opzione non può essere usata in combinazione con altre opzioni.</p> | 



## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
