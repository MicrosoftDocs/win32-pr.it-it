---
description: 'Altre informazioni su: membri di ColumnStream'
title: 'Membri di ColumnStream '
TOCTitle: ColumnStream members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.ColumnStream
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnstream_members(v=EXCHG.10)
ms:contentKeyID: 55101147
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 9f35c0e000329bc98e2f9fd5873cd724516271d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104552189"
---
# <a name="columnstream-members"></a>Membri di ColumnStream 

Includi membri protetti  
Includi membri ereditati  

Questa classe fornisce un'interfaccia di flusso a una colonna con valore Long, ovvero una colonna di tipo [LongBinary](./jet-coltyp-enumeration.md) o [LONGTEXT](./jet-coltyp-enumeration.md).

Il tipo [ColumnStream](./columnstream-class.md) espone i membri seguenti.

## <a name="constructors"></a>Costruttori

<table>
<thead>
<tr class="header">
<th> </th>
<th>Nome</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><a href="dn334142(v=exchg.10).md">ColumnStream</a></td>
<td>Inizializza una nuova istanza della classe ColumnStream.</td>
</tr>
</tbody>
</table>


Inizio

## <a name="properties"></a>Proprietà

<table>
<thead>
<tr class="header">
<th> </th>
<th>Nome</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn334201(v=exchg.10).md">CanRead</a></td>
<td>Ottiene un valore che indica se il flusso supporta la lettura. Esegue l'override di <a href="/dotnet/api/system.io.stream.canread#System_IO_Stream_CanRead">Stream. CanRead</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn334153(v=exchg.10).md">CanSeek</a></td>
<td>Ottiene un valore che indica se il flusso supporta la ricerca. Esegue l'override di <a href="/dotnet/api/system.io.stream.canseek#System_IO_Stream_CanSeek">Stream. CanSeek</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="/dotnet/api/system.io.stream.cantimeout#System_IO_Stream_CanTimeout">CanTimeout</a></td>
<td>Ereditato dal <a href="/dotnet/api/system.io.stream">flusso</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn334204(v=exchg.10).md">CanWrite</a></td>
<td>Ottiene un valore che indica se il flusso supporta la scrittura. Esegue l'override di <a href="/dotnet/api/system.io.stream.canwrite#System_IO_Stream_CanWrite">Stream. CanWrite</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn334159(v=exchg.10).md">Itag</a></td>
<td>Ottiene o imposta il ITag della colonna.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn334205(v=exchg.10).md">Length</a></td>
<td>Ottiene la lunghezza corrente del flusso. Esegue l'override di <a href="/dotnet/api/system.io.stream.length#System_IO_Stream_Length">Stream. length</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn334161(v=exchg.10).md">Position</a></td>
<td>Ottiene o imposta la posizione corrente nel flusso. (Esegue l'override di <a href="/dotnet/api/system.io.stream.position#System_IO_Stream_Position">Stream. Position</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="/dotnet/api/system.io.stream.readtimeout#System_IO_Stream_ReadTimeout">ReadTimeout</a></td>
<td>Ereditato dal <a href="/dotnet/api/system.io.stream">flusso</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="/dotnet/api/system.io.stream.writetimeout#System_IO_Stream_WriteTimeout">WriteTimeout</a></td>
<td>Ereditato dal <a href="/dotnet/api/system.io.stream">flusso</a>.</td>
</tr>
</tbody>
</table>


Inizio

## <a name="methods"></a>Metodi

<table>
<thead>
<tr class="header">
<th> </th>
<th>Nome</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><a href="/dotnet/api/system.io.stream.beginread#System_IO_Stream_BeginRead_System_Byte___System_Int32_System_Int32_System_AsyncCallback_System_Object_">BeginRead</a></td>
<td>Ereditato dal <a href="/dotnet/api/system.io.stream">flusso</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><a href="/dotnet/api/system.io.stream.beginwrite#System_IO_Stream_BeginWrite_System_Byte___System_Int32_System_Int32_System_AsyncCallback_System_Object_">BeginWrite</a></td>
<td>Ereditato dal <a href="/dotnet/api/system.io.stream">flusso</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><a href="/dotnet/api/system.io.stream.close#System_IO_Stream_Close">Close</a></td>
<td>Ereditato dal <a href="/dotnet/api/system.io.stream">flusso</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><a href="/dotnet/api/system.marshalbyrefobject.createobjref#System_MarshalByRefObject_CreateObjRef_System_Type_">CreateObjRef</a></td>
<td>Ereditato da <a href="/dotnet/api/system.marshalbyrefobject">MarshalByRefObject</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.io.stream.createwaithandle#System_IO_Stream_CreateWaitHandle">CreateWaitHandle</a></td>
<td><strong>Obsoleto.</strong> Ereditato dal <a href="/dotnet/api/system.io.stream">flusso</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><a href="/dotnet/api/system.io.stream.dispose#System_IO_Stream_Dispose">Dispose ()</a></td>
<td>Ereditato dal <a href="/dotnet/api/system.io.stream">flusso</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.io.stream.dispose#System_IO_Stream_Dispose_System_Boolean_">Dispose (valore booleano)</a></td>
<td>Ereditato dal <a href="/dotnet/api/system.io.stream">flusso</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><a href="/dotnet/api/system.io.stream.endread#System_IO_Stream_EndRead_System_IAsyncResult_">EndRead</a></td>
<td>Ereditato dal <a href="/dotnet/api/system.io.stream">flusso</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><a href="/dotnet/api/system.io.stream.endwrite#System_IO_Stream_EndWrite_System_IAsyncResult_">EndWrite</a></td>
<td>Ereditato dal <a href="/dotnet/api/system.io.stream">flusso</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">È uguale a</a></td>
<td>Ereditato da <a href="/dotnet/api/system.object">Object</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></td>
<td>Ereditato da <a href="/dotnet/api/system.object">Object</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><a href="dn334193(v=exchg.10).md">Svuotamento</a></td>
<td>Svuotare il flusso. Esegue l'override di <a href="/dotnet/api/system.io.stream.flush#System_IO_Stream_Flush">Stream. Flush ()</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></td>
<td>Ereditato da <a href="/dotnet/api/system.object">Object</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><a href="/dotnet/api/system.marshalbyrefobject.getlifetimeservice#System_MarshalByRefObject_GetLifetimeService">GetLifetimeService</a></td>
<td>Ereditato da <a href="/dotnet/api/system.marshalbyrefobject">MarshalByRefObject</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></td>
<td>Ereditato da <a href="/dotnet/api/system.object">Object</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><a href="/dotnet/api/system.marshalbyrefobject.initializelifetimeservice#System_MarshalByRefObject_InitializeLifetimeService">InitializeLifetimeService</a></td>
<td>Ereditato da <a href="/dotnet/api/system.marshalbyrefobject">MarshalByRefObject</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone ()</a></td>
<td>Ereditato da <a href="/dotnet/api/system.object">Object</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.marshalbyrefobject.memberwiseclone#System_MarshalByRefObject_MemberwiseClone_System_Boolean_">MemberwiseClone (booleano)</a></td>
<td>Ereditato da <a href="/dotnet/api/system.marshalbyrefobject">MarshalByRefObject</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><a href="dn334198(v=exchg.10).md">Lettura</a></td>
<td>Legge una sequenza di byte dal flusso corrente e fa avanzare la posizione nel flusso del numero di byte letti. Esegue l'override di <a href="/dotnet/api/system.io.stream.read#System_IO_Stream_Read_System_Byte___System_Int32_System_Int32_">Stream. Read ([], Int32, Int32)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><a href="/dotnet/api/system.io.stream.readbyte#System_IO_Stream_ReadByte">ReadByte</a></td>
<td>Ereditato dal <a href="/dotnet/api/system.io.stream">flusso</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><a href="dn334154(v=exchg.10).md">Seek</a></td>
<td>Imposta la posizione all'interno del flusso corrente. (Esegue l'override <a href="/dotnet/api/system.io.stream.seek#System_IO_Stream_Seek_System_Int64_System_IO_SeekOrigin_">di Stream. Seek (Int64, SeekOrigin)</a>).</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><a href="dn334196(v=exchg.10).md">SetLength</a></td>
<td>Imposta la lunghezza del flusso. Esegue l'override di <a href="/dotnet/api/system.io.stream.setlength#System_IO_Stream_SetLength_System_Int64_">Stream. selength (Int64)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><a href="dn334149(v=exchg.10).md">ToString</a></td>
<td>Restituisce una <a href="/dotnet/api/system.string">stringa</a> che rappresenta l'oggetto <a href="dn334143(v=exchg.10).md">ColumnStream</a>corrente. Esegue l'override di <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><a href="dn334197(v=exchg.10).md">Scrittura</a></td>
<td>Scrive una sequenza di byte nel flusso corrente e fa avanzare la posizione corrente nel flusso del numero di byte scritti. Esegue l'override <a href="/dotnet/api/system.io.stream.write#System_IO_Stream_Write_System_Byte___System_Int32_System_Int32_">di Stream. Write ([], Int32, Int32)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><a href="/dotnet/api/system.io.stream.writebyte#System_IO_Stream_WriteByte_System_Byte_">WriteByte</a></td>
<td>Ereditato dal <a href="/dotnet/api/system.io.stream">flusso</a>.</td>
</tr>
</tbody>
</table>


Inizio

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe ColumnStream](./columnstream-class.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
