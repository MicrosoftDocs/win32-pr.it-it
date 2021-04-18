---
description: 'Altre informazioni su: Enumerazione OpenTableGrbit'
title: Enumerazione OpenTableGrbit
TOCTitle: OpenTableGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.OpenTableGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.opentablegrbit(v=EXCHG.10)
ms:contentKeyID: 39510721
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.NoCache
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.DenyWrite
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.DenyRead
- Microsoft.Isam.Esent.Interop.OpenTableGrbit
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.Updatable
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.Preread
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass9
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass15
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass6
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass14
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass3
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass8
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass7
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.Sequential
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass5
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass2
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.ReadOnly
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass4
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.None
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass10
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass13
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass12
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass1
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.PermitDDL
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass11
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass1
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass11
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass14
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.Sequential
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass2
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass5
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass8
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.DenyRead
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.DenyWrite
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.PermitDDL
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass10
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass12
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass3
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.NoCache
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass9
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.Updatable
- Microsoft.Isam.Esent.Interop.OpenTableGrbit
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.None
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass4
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass7
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.Preread
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.ReadOnly
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass13
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass15
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass6
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: dfb2d75fc17e37dc669acf1fd84f38c957d467f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313089"
---
# <a name="opentablegrbit-enumeration"></a>Enumerazione OpenTableGrbit

Opzioni per JetOpenTable.

Questa enumerazione ha un attributo [FlagsAttribute](/dotnet/api/system.flagsattribute) che consente una combinazione bit per bit dei valori del relativo membro.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration OpenTableGrbit
'Usage
Dim instance As OpenTableGrbit
```

``` csharp
[FlagsAttribute]
public enum OpenTableGrbit
```

## <a name="members"></a>Members

<table>
<thead>
<tr class="header">
<th></th>
<th>Nome del membro</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td>nessuno</td>
<td>Opzioni predefinite.</td>
</tr>
<tr class="even">
<td></td>
<td>DenyWrite</td>
<td>Questa tabella non può essere aperta per l'accesso in scrittura da un'altra sessione.</td>
</tr>
<tr class="odd">
<td></td>
<td>DenyRead</td>
<td>Non è possibile aprire questa tabella per l'accesso in lettura da un'altra sessione.</td>
</tr>
<tr class="even">
<td></td>
<td>ReadOnly</td>
<td>Richiedere l'accesso in sola lettura alla tabella.</td>
</tr>
<tr class="odd">
<td></td>
<td>Aggiornabile</td>
<td>Richiedere l'accesso in scrittura alla tabella.</td>
</tr>
<tr class="even">
<td></td>
<td>PermitDDL</td>
<td>Consente le modifiche DDL a una tabella contrassegnata come FixedDDL. Questa opzione deve essere usata con DenyRead.</td>
</tr>
<tr class="odd">
<td></td>
<td>NoCache</td>
<td>Non memorizzare nella cache le pagine per questa tabella.</td>
</tr>
<tr class="even">
<td></td>
<td>Prelettura</td>
<td>Fornisce un suggerimento che la tabella non è probabilmente nella cache del buffer e che la pre-lettura può essere utile per le prestazioni.</td>
</tr>
<tr class="odd">
<td></td>
<td>Sequenziale</td>
<td>Si supponga un modello di accesso sequenziale e le pagine di database di prelettura.</td>
</tr>
<tr class="even">
<td></td>
<td>TableClass1</td>
<td>La tabella appartiene alla classe stats 1.</td>
</tr>
<tr class="odd">
<td></td>
<td>TableClass2</td>
<td>La tabella appartiene alla classe stats 2.</td>
</tr>
<tr class="even">
<td></td>
<td>TableClass3</td>
<td>La tabella appartiene alla classe stats 3.</td>
</tr>
<tr class="odd">
<td></td>
<td>TableClass4</td>
<td>La tabella appartiene alla classe stats 4.</td>
</tr>
<tr class="even">
<td></td>
<td>TableClass5</td>
<td>La tabella appartiene alla classe stats 5.</td>
</tr>
<tr class="odd">
<td></td>
<td>TableClass6</td>
<td>La tabella appartiene alla classe stats 6.</td>
</tr>
<tr class="even">
<td></td>
<td>TableClass7</td>
<td>La tabella appartiene alla classe stats 7.</td>
</tr>
<tr class="odd">
<td></td>
<td>TableClass8</td>
<td>La tabella appartiene alla classe stats 8.</td>
</tr>
<tr class="even">
<td></td>
<td>TableClass9</td>
<td>La tabella appartiene alla classe stats 9.</td>
</tr>
<tr class="odd">
<td></td>
<td>TableClass10</td>
<td>La tabella appartiene alla classe stats 10.</td>
</tr>
<tr class="even">
<td></td>
<td>TableClass11</td>
<td>La tabella appartiene alla classe stats 11.</td>
</tr>
<tr class="odd">
<td></td>
<td>TableClass12</td>
<td>La tabella appartiene alla classe stats 12.</td>
</tr>
<tr class="even">
<td></td>
<td>TableClass13</td>
<td>La tabella appartiene alla classe stats 13.</td>
</tr>
<tr class="odd">
<td></td>
<td>TableClass14</td>
<td>La tabella appartiene alla classe stats 14.</td>
</tr>
<tr class="even">
<td></td>
<td>TableClass15</td>
<td>La tabella appartiene alla classe stats 15.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
