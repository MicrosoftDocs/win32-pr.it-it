---
description: 'Altre informazioni su: JET_CBTYP'
title: JET_CBTYP
TOCTitle: JET_CBTYP
ms:assetid: babbfa11-01a7-477b-a525-cff27a983b60
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294071(v=EXCHG.10)
ms:contentKeyID: 32765686
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0b01bafad091ed17e018793ea701596aef6d0d72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317399"
---
# <a name="jet_cbtyp"></a>JET_CBTYP


_**Si applica a:** Windows | Windows Server_

## <a name="jet_cbtyp"></a>JET_CBTYP

Il **JET_CBTYP** gruppo di costanti descrive tutti i punti possibili in un'operazione che il motore di database invierà una notifica a un'applicazione chiamando la funzione di CALLBACK di [JET_CALLBACK](./jet-callback-callback-function.md) . Il motore di database passa una di queste costanti nel parametro *cbtyp* della funzione di callback. Il significato degli altri parametri passati dal motore di database in questa chiamata dipende dalla **JET_CBTYP** specifica passata.

**Windows XP:**  Il gruppo **JET_CBTYP** di costanti è stato introdotto in Windows XP.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Costante/valore</p></th>
<th><p>Descrizione</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_cbtypNull<br />
0x00000000</p></td>
<td><p>Questo callback è riservato e sempre considerato non valido.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbtypFinalize<br />
0x00000001</p></td>
<td><p>Questo callback è riservato per un uso futuro.</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbtypBeforeInsert<br />
0x00000002</p></td>
<td><p>Questo callback si verificherà immediatamente prima dell'inserimento di un nuovo record in una tabella tramite una chiamata a <a href="gg269288(v=exchg.10).md">JetUpdate</a>.</p>
<p>Il puntatore a funzione per questo motivo di callback viene passato a <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> per mezzo di <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> o viene configurato in fase di esecuzione per mezzo di <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>. Per ulteriori informazioni, vedere <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> o <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</p>
<p>I parametri di callback avranno i valori seguenti:</p>
<ul>
<li><p><em>sesid</em>: sessione in cui è presente il record da inserire.</p></li>
<li><p><em>dbid</em>: ID database della tabella che contiene il record da inserire.</p></li>
<li><p><em>TableID</em>: cursore che ha preparato il nuovo record da inserire. È importante notare che in questo momento il valore di qualsiasi versione o di colonne con incremento automatico potrebbe non essere corretto.</p></li>
<li><p><em>pvArg1</em>: <strong>null</strong></p></li>
<li><p><em>pvArg2</em>: <strong>null</strong></p></li>
<li><p><em>pvContext</em>: puntatore di contesto passato a <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> o <strong>null</strong>.</p></li>
<li><p><em>ulUnused</em>: <strong>null</strong> se il callback restituisce un errore, l'operazione originata dal callback avrà esito negativo con l'errore.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_cbtypAfterInsert<br />
0x00000004</p></td>
<td><p>Questo callback si verificherà subito dopo l'inserimento di un nuovo record in una tabella tramite una chiamata a <a href="gg269288(v=exchg.10).md">JetUpdate</a> ma prima che <a href="gg269288(v=exchg.10).md">JetUpdate</a> torni al chiamante.</p>
<p>Il puntatore a funzione per questo motivo di callback viene passato a <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> per mezzo di <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> o viene configurato in fase di esecuzione per mezzo di <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>. Per ulteriori informazioni, vedere <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> o <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</p>
<p>I parametri di callback avranno i valori seguenti:</p>
<ul>
<li><p><em>sesid</em>: la sessione che contiene il record appena inserito.</p></li>
<li><p><em>dbid</em>: ID database della tabella che contiene il record appena inserito.</p></li>
<li><p><em>TableID</em>: cursore della tabella in cui è stato appena inserito il record. Si noti che il cursore è ancora posizionato sulla stessa voce di indice in cui si trovava nel callback di prima dell'inserimento. Si noti inoltre che questa voce di indice potrebbe non essere correlata in alcun modo al record da inserire.</p></li>
<li><p><em>pvArg1</em>: <strong>null</strong></p></li>
<li><p><em>pvArg2</em>: <strong>null</strong></p></li>
<li><p><em>pvContext</em>: puntatore di contesto passato a <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> o <strong>null</strong>.</p></li>
<li><p><em>ulUnused</em>: <strong>null</strong> se il callback restituisce un errore, verrà ignorato.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_cbtypBeforeReplace<br />
0x00000008</p></td>
<td><p>Questo callback si verificherà immediatamente prima di un record esistente in una tabella modificata da una chiamata a <a href="gg269288(v=exchg.10).md">JetUpdate</a>.</p>
<p>Il puntatore a funzione per questo motivo di callback viene passato a <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> per mezzo di <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> o viene configurato in fase di esecuzione per mezzo di <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>. Per ulteriori informazioni, vedere <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> o <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</p>
<p>I parametri di callback avranno i valori seguenti:</p>
<ul>
<li><p><em>sesid</em>: la sessione in cui è presente il record da modificare.</p></li>
<li><p><em>dbid</em>: ID database della tabella che contiene il record da modificare.</p></li>
<li><p><em>TableID</em>: cursore posizionato in corrispondenza di una voce di indice associata al record da modificare. È importante notare che in questo momento il valore di qualsiasi versione o di colonne con incremento automatico potrebbe non essere corretto.</p></li>
<li><p><em>pvArg1</em>: <strong>null</strong></p></li>
<li><p><em>pvArg2</em>: <strong>null</strong></p></li>
<li><p><em>pvContext</em>: puntatore di contesto passato a <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> o <strong>null</strong>.</p></li>
<li><p><em>ulUnused</em>: <strong>null</strong> se il callback restituisce un errore, l'operazione originata dal callback avrà esito negativo con l'errore.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_cbtypAfterReplace<br />
0x00000010</p></td>
<td><p>Questo callback si verifica subito dopo la modifica di un record esistente in una tabella da una chiamata a <a href="gg269288(v=exchg.10).md">JetUpdate</a> , ma prima che <a href="gg269288(v=exchg.10).md">JetUpdate</a> torni al chiamante.</p>
<p>Il puntatore a funzione per questo motivo di callback viene passato a <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> per mezzo di <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> o viene configurato in fase di esecuzione per mezzo di <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>. Per ulteriori informazioni, vedere <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> o <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</p>
<p>I parametri di callback avranno i valori seguenti:</p>
<ul>
<li><p><em>sesid</em>: la sessione che contiene il record appena modificato.</p></li>
<li><p><em>dbid</em>: ID database della tabella che contiene il record appena modificato.</p></li>
<li><p><em>TableID</em>: cursore posizionato in corrispondenza di una voce di indice associata al record appena modificato.</p></li>
<li><p><em>pvArg1</em>: <strong>null</strong></p></li>
<li><p><em>pvArg2</em>: <strong>null</strong></p></li>
<li><p><em>pvContext</em>: puntatore di contesto passato a <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> o <strong>null</strong>.</p></li>
<li><p><em>ulUnused</em>: <strong>null</strong> se il callback restituisce un errore, verrà ignorato.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_cbtypBeforeDelete<br />
0x00000020</p></td>
<td><p>Questo callback si verificherà immediatamente prima che un record esistente in una tabella venga eliminato da una chiamata a <a href="gg269315(v=exchg.10).md">JetDelete</a>.</p>
<p>Il puntatore a funzione per questo motivo di callback viene passato a <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> per mezzo di <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> o viene configurato in fase di esecuzione per mezzo di <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>. Per ulteriori informazioni, vedere <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> o <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</p>
<p>I parametri di callback avranno i valori seguenti:</p>
<ul>
<li><p><em>sesid</em>: sessione in cui è presente il record da eliminare.</p></li>
<li><p><em>dbid</em>: ID database della tabella che contiene il record da eliminare.</p></li>
<li><p><em>TableID</em>: cursore posizionato in corrispondenza di una voce di indice associata al record da eliminare.</p></li>
<li><p><em>pvArg1</em>: <strong>null</strong></p></li>
<li><p><em>pvArg2</em>: <strong>null</strong></p></li>
<li><p><em>pvContext</em>: puntatore di contesto passato a <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> o <strong>null</strong>.</p></li>
<li><p><em>ulUnused</em>: <strong>null</strong> se il callback restituisce un errore, l'operazione originata dal callback avrà esito negativo con l'errore.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_cbtypAfterDelete<br />
0x00000040</p></td>
<td><p>Questo callback si verificherà subito dopo l'eliminazione di un record esistente in una tabella da una chiamata a <a href="gg269315(v=exchg.10).md">JetDelete</a> ma prima che <a href="gg269315(v=exchg.10).md">JetDelete</a> torni al chiamante.</p>
<p>Il puntatore a funzione per questo motivo di callback viene passato a <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> per mezzo di <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> o viene configurato in fase di esecuzione per mezzo di <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>. Per ulteriori informazioni, vedere <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> o <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>.</p>
<p>I parametri di callback avranno i valori seguenti:</p>
<ul>
<li><p><em>sesid</em>: la sessione in cui è stato appena eliminato il record.</p></li>
<li><p><em>dbid</em>: ID database della tabella che contiene il record appena eliminato.</p></li>
<li><p><em>TableID</em>: cursore posizionato in corrispondenza di una voce di indice associata al record appena eliminato.</p></li>
<li><p><em>pvArg1</em>: <strong>null</strong></p></li>
<li><p><em>pvArg2</em>: <strong>null</strong></p></li>
<li><p><em>pvContext</em>: puntatore di contesto passato a <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a> o <strong>null</strong>.</p></li>
<li><p><em>ulUnused</em>: <strong>null</strong></p></li>
</ul>
<p>Se un errore viene restituito dal callback, verrà ignorato.</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbtypUserDefinedDefaultValue<br />
0x00000080</p></td>
<td><p>Questo callback si verifica quando il motore deve recuperare il valore predefinito definito dall'utente di una colonna dall'applicazione. Questo callback è essenzialmente un'implementazione limitata di <a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a> valutata dall'applicazione. Per un valore predefinito definito dall'utente può essere restituito un massimo di un valore di colonna.</p>
<p>Il puntatore a funzione per questo motivo di callback viene passato a <a href="gg294122(v=exchg.10).md">JetAddColumn</a> per mezzo di una struttura <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> o passato a <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> tramite una struttura di <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> in una struttura di <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> in una struttura <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> .</p>
<p>I parametri di callback avranno i valori seguenti:</p>
<ul>
<li><p><em>sesid</em>: la sessione che sta calcolando il valore predefinito definito dall'utente</p></li>
<li><p><em>dbid</em>: ID database della tabella che contiene il valore predefinito definito dall'utente</p></li>
<li><p><em>TableID</em>: cursore posizionato sul record per il quale viene recuperato il valore predefinito definito dall'utente</p></li>
<li><p><em>pvArg1</em>: buffer di output per il valore predefinito definito dall'utente</p></li>
<li><p><em>pvArg2</em>: in input, si tratta della dimensione del buffer di output. Nell'output corrisponde alla dimensione effettiva del valore predefinito definito dall'utente. in entrambi i casi, la dimensione è una Unsigned Integer a 32 bit.</p></li>
<li><p><em>pvContext</em>: puntatore a un buffer contenente i dati utente specificati nella struttura <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> quando è stata creata la colonna oppure null se non è stato specificato alcun contesto.</p></li>
<li><p><em>ulUnused</em>: ID di colonna della colonna per cui viene recuperato il valore predefinito definito dall'utente.</p></li>
</ul>
<p>Se viene restituito un errore dal callback, l'operazione di origine del callback avrà esito negativo con l'errore.</p>
<p>Se JET_wrnBufferTruncated viene restituito dal callback, l'operazione continuerà, ma l'intero valore non viene recuperato durante il callback.</p>
<p>Se JET_wrnColumnNull viene restituito dal callback, l'operazione continuerà, ma il valore predefinito definito dall'utente per la colonna è NULL.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbtypOnlineDefragCompleted<br />
0x00000100</p></td>
<td><p>Questo callback si verifica quando la deframmentazione in linea di un database iniziata da <a href="gg269317(v=exchg.10).md">JetDefragment</a> è stata interrotta a causa del completamento del processo o del raggiungimento del limite di tempo.</p>
<p>Il puntatore a funzione per questo motivo di callback viene passato a <a href="gg269317(v=exchg.10).md">JetDefragment</a>. Per ulteriori informazioni, vedere <a href="gg269317(v=exchg.10).md">JetDefragment</a>.</p>
<p>I parametri di callback avranno i valori seguenti:</p>
<ul>
<li><p><em>sesid</em>: sessione utilizzata per eseguire la deframmentazione in linea del database o JET_sesidNil per un file di streaming.</p></li>
<li><p><em>dbid</em>: ID del database da deframmentare o JET_dbidNil per un file di streaming.</p></li>
<li><p><em>TableID</em>: JET_tableidNil</p></li>
<li><p><em>pvArg1</em>: <strong>null</strong></p></li>
<li><p><em>pvArg2</em>: <strong>null</strong></p></li>
<li><p><em>pvContext</em>: <strong>null</strong></p></li>
<li><p><em>ulUnused</em>: <strong>null</strong></p></li>
</ul>
<p>Se un errore viene restituito dal callback, verrà ignorato.</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbtypFreeCursorLS<br />
0x00000200</p></td>
<td><p>Questo callback si verifica quando l'applicazione deve eseguire la pulizia dell'handle di contesto per l'archiviazione locale associata a un cursore rilasciato dal motore di database. Per ulteriori informazioni, vedere <a href="gg269243(v=exchg.10).md">JetSetLS</a>.</p>
<p>Il puntatore a funzione per questo motivo di callback viene configurato per mezzo di <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con <a href="gg269310(v=exchg.10).md">JET_paramRuntimeCallback</a>.</p>
<p>I parametri di callback avranno i valori seguenti:</p>
<ul>
<li><p><em>sesid</em>: JET_sesidNil</p></li>
<li><p><em>dbid</em>: JET_dbidNil</p></li>
<li><p><em>TableID</em>: JET_tableidNil</p></li>
<li><p><em>pvArg1</em>: set di handle di contesto con <a href="gg269243(v=exchg.10).md">JetSetLS</a></p></li>
<li><p><em>pvArg2</em>: <strong>null</strong></p></li>
<li><p><em>pvContext</em>: <strong>null</strong></p></li>
<li><p><em>ulUnused</em>: <strong>null</strong></p></li>
</ul>
<p>Se un errore viene restituito dal callback, verrà ignorato.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbtypFreeTableLS<br />
0x00000400</p></td>
<td><p>Questo callback si verificherà come il risultato della necessità che l'applicazione ripulisca l'handle di contesto per l'archiviazione locale associata a una tabella rilasciata dal motore di database. Per ulteriori informazioni, vedere <a href="gg269243(v=exchg.10).md">JetSetLS</a>.</p>
<p>Il puntatore a funzione per questo motivo di callback viene configurato per mezzo di <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con <a href="gg269310(v=exchg.10).md">JET_paramRuntimeCallback</a>.</p>
<p>I parametri di callback avranno i valori seguenti:</p>
<ul>
<li><p><em>sesid</em>: JET_sesidNil</p></li>
<li><p><em>dbid</em>: JET_dbidNil</p></li>
<li><p><em>TableID</em>: JET_tableidNil</p></li>
<li><p><em>pvArg1</em>: set di handle di contesto con <a href="gg269243(v=exchg.10).md">JetSetLS</a>.</p></li>
<li><p><em>pvArg2</em>: <strong>null</strong></p></li>
<li><p><em>pvContext</em>: <strong>null</strong></p></li>
<li><p><em>ulUnused</em>: <strong>null</strong></p></li>
</ul>
<p>Se un errore viene restituito dal callback, verrà ignorato.</p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a>Requisiti

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Richiede Windows Vista o Windows XP.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Richiede Windows Server 2008 o Windows Server 2003.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Intestazione</strong></p></td>
<td><p>Dichiarata in esent. h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Vedere anche

[JET_CALLBACK](./jet-callback-callback-function.md)
