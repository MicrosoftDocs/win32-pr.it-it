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
ms.openlocfilehash: fa797fac58b0a2663c918e7fef739c6c5ab536dcfa9dc91be13b8196aed5ef43
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119945911"
---
# <a name="jet_cbtyp"></a>JET_CBTYP


_**Si applica a:** Windows | Windows Server_

## <a name="jet_cbtyp"></a>JET_CBTYP

Il **JET_CBTYP** di costanti descrive tutti i punti possibili in un'operazione a cui il motore di database invierà una notifica a un'applicazione chiamando la JET_CALLBACK [di](./jet-callback-callback-function.md) callback. Il motore di database passa una di queste costanti nel *parametro cbtyp* della funzione di callback. Il significato degli altri parametri passati dal motore di database in questa chiamata dipende dal valore **JET_CBTYP** passato.

**Windows XP:**  Il **JET_CBTYP** di costanti è stato introdotto in Windows XP.

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
<td><p>Questo callback è riservato e considerato sempre non valido.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbtypFinalize<br />
0x00000001</p></td>
<td><p>Questo callback è riservato per un uso futuro.</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbtypBeforeInsert<br />
0x00000002</p></td>
<td><p>Questo callback si verificherà subito prima dell'inserimento di un nuovo record in una tabella tramite una chiamata a <a href="gg269288(v=exchg.10).md">JetUpdate</a>.</p>
<p>Il puntatore a funzione per questo motivo di callback <a href="gg294146(v=exchg.10).md"></a> viene passato a <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> tramite JET_TABLECREATE o viene configurato in fase di esecuzione tramite <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>. Per altre informazioni, vedere <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> <a href="gg269175(v=exchg.10).md">o JetRegisterCallback</a>.</p>
<p>I parametri di callback avranno i valori seguenti:</p>
<ul>
<li><p><em>sesid:</em>sessione con il record da inserire.</p></li>
<li><p><em>dbid:</em>ID database della tabella che contiene il record da inserire.</p></li>
<li><p><em>tableid:</em>cursore che ha preparato il nuovo record da inserire. È importante notare che il valore di qualsiasi colonna di versione o incremento automatico potrebbe non essere corretto in questo momento.</p></li>
<li><p><em>pvArg1:</em> <strong>NULL</strong></p></li>
<li><p><em>pvArg2:</em> <strong>NULL</strong></p></li>
<li><p><em>pvContext:</em>puntatore di contesto passato <a href="gg269175(v=exchg.10).md">a JetRegisterCallback</a> o <strong>NULL.</strong></p></li>
<li><p><em>ulUnused:</em> <strong>NULL Se</strong> il callback restituisce un errore, l'operazione che ha origine il callback avrà esito negativo con tale errore.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_cbtypAfterInsert<br />
0x00000004</p></td>
<td><p>Questo callback si verificherà subito dopo l'inserimento di un nuovo record in una tabella da una chiamata a <a href="gg269288(v=exchg.10).md">JetUpdate,</a> ma prima che <a href="gg269288(v=exchg.10).md">JetUpdate</a> restituisca al chiamante.</p>
<p>Il puntatore a funzione per questo motivo di callback <a href="gg294146(v=exchg.10).md"></a> viene passato a <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> tramite JET_TABLECREATE o viene configurato in fase di esecuzione tramite <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>. Per altre informazioni, vedere <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> <a href="gg269175(v=exchg.10).md">o JetRegisterCallback</a>.</p>
<p>I parametri di callback avranno i valori seguenti:</p>
<ul>
<li><p><em>sesid:</em>sessione con il record appena inserito.</p></li>
<li><p><em>dbid:</em>ID database della tabella che contiene il record appena inserito.</p></li>
<li><p><em>tableid:</em>cursore sulla tabella in cui è stato appena inserito il record. Si noti che il cursore è ancora posizionato sulla stessa voce di indice del callback prima dell'inserimento. Si noti inoltre che questa voce di indice potrebbe non essere correlata in alcun modo al record inserito.</p></li>
<li><p><em>pvArg1:</em> <strong>NULL</strong></p></li>
<li><p><em>pvArg2:</em> <strong>NULL</strong></p></li>
<li><p><em>pvContext:</em>puntatore di contesto passato <a href="gg269175(v=exchg.10).md">a JetRegisterCallback</a> o <strong>NULL.</strong></p></li>
<li><p><em>ulUnused:</em> <strong>NULL Se</strong> un errore viene restituito dal callback, verrà ignorato.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_cbtypBeforeReplace<br />
0x00000008</p></td>
<td><p>Questo callback si verificherà subito prima che un record esistente in una tabella venga modificato da una chiamata a <a href="gg269288(v=exchg.10).md">JetUpdate</a>.</p>
<p>Il puntatore a funzione per questo motivo di callback <a href="gg294146(v=exchg.10).md"></a> viene passato a <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> tramite JET_TABLECREATE o viene configurato in fase di esecuzione tramite <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>. Per altre informazioni, vedere <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> <a href="gg269175(v=exchg.10).md">o JetRegisterCallback</a>.</p>
<p>I parametri di callback avranno i valori seguenti:</p>
<ul>
<li><p><em>sesid:</em>sessione con il record da modificare.</p></li>
<li><p><em>dbid:</em>ID database della tabella che contiene il record da modificare.</p></li>
<li><p><em>tableid:</em>cursore posizionato su una voce di indice associata al record da modificare. È importante notare che il valore di qualsiasi colonna di versione o incremento automatico potrebbe non essere corretto in questo momento.</p></li>
<li><p><em>pvArg1:</em> <strong>NULL</strong></p></li>
<li><p><em>pvArg2:</em> <strong>NULL</strong></p></li>
<li><p><em>pvContext:</em>puntatore di contesto passato <a href="gg269175(v=exchg.10).md">a JetRegisterCallback</a> o <strong>NULL.</strong></p></li>
<li><p><em>ulUnused:</em> <strong>NULL Se</strong> il callback restituisce un errore, l'operazione che ha origine il callback avrà esito negativo con tale errore.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_cbtypAfterReplace<br />
0x00000010</p></td>
<td><p>Questo callback si verificherà subito dopo che un record esistente in una tabella è stato modificato da una chiamata a <a href="gg269288(v=exchg.10).md">JetUpdate</a> ma prima che <a href="gg269288(v=exchg.10).md">JetUpdate restituiva</a> al chiamante.</p>
<p>Il puntatore a funzione per questo motivo di callback <a href="gg294146(v=exchg.10).md"></a> viene passato a <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> tramite JET_TABLECREATE o viene configurato in fase di esecuzione tramite <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>. Per altre informazioni, vedere <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> <a href="gg269175(v=exchg.10).md">o JetRegisterCallback</a>.</p>
<p>I parametri di callback avranno i valori seguenti:</p>
<ul>
<li><p><em>sesid:</em>sessione con il record appena modificato.</p></li>
<li><p><em>dbid:</em>ID database della tabella che contiene il record appena modificato.</p></li>
<li><p><em>tableid:</em>cursore posizionato su una voce di indice associata al record appena modificato.</p></li>
<li><p><em>pvArg1:</em> <strong>NULL</strong></p></li>
<li><p><em>pvArg2:</em> <strong>NULL</strong></p></li>
<li><p><em>pvContext:</em>puntatore di contesto passato <a href="gg269175(v=exchg.10).md">a JetRegisterCallback</a> o <strong>NULL.</strong></p></li>
<li><p><em>ulUnused:</em> <strong>NULL Se</strong> un errore viene restituito dal callback, verrà ignorato.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_cbtypBeforeDelete<br />
0x00000020</p></td>
<td><p>Questo callback si verificherà poco prima che un record esistente in una tabella venga eliminato da una chiamata a <a href="gg269315(v=exchg.10).md">JetDelete.</a></p>
<p>Il puntatore a funzione per questo motivo di callback <a href="gg294146(v=exchg.10).md"></a> viene passato a <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> tramite JET_TABLECREATE o viene configurato in fase di esecuzione tramite <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>. Per altre informazioni, vedere <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> <a href="gg269175(v=exchg.10).md">o JetRegisterCallback</a>.</p>
<p>I parametri di callback avranno i valori seguenti:</p>
<ul>
<li><p><em>sesid:</em>sessione con il record da eliminare.</p></li>
<li><p><em>dbid:</em>ID database della tabella che contiene il record da eliminare.</p></li>
<li><p><em>tableid:</em>cursore posizionato su una voce di indice associata al record da eliminare.</p></li>
<li><p><em>pvArg1:</em> <strong>NULL</strong></p></li>
<li><p><em>pvArg2:</em> <strong>NULL</strong></p></li>
<li><p><em>pvContext:</em>puntatore di contesto passato <a href="gg269175(v=exchg.10).md">a JetRegisterCallback</a> o <strong>NULL.</strong></p></li>
<li><p><em>ulUnused:</em> <strong>NULL Se</strong> il callback restituisce un errore, l'operazione che ha origine il callback avrà esito negativo con tale errore.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_cbtypAfterDelete<br />
0x00000040</p></td>
<td><p>Questo callback si verificherà subito dopo che un record esistente in una tabella è stato eliminato da una chiamata a <a href="gg269315(v=exchg.10).md">JetDelete</a> ma prima <a href="gg269315(v=exchg.10).md">che JetDelete</a> restituisca al chiamante.</p>
<p>Il puntatore a funzione per questo motivo di callback <a href="gg294146(v=exchg.10).md"></a> viene passato a <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> tramite JET_TABLECREATE o viene configurato in fase di esecuzione tramite <a href="gg269175(v=exchg.10).md">JetRegisterCallback</a>. Per altre informazioni, vedere <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> <a href="gg269175(v=exchg.10).md">o JetRegisterCallback</a>.</p>
<p>I parametri di callback avranno i valori seguenti:</p>
<ul>
<li><p><em>sesid:</em>sessione con il record appena eliminato.</p></li>
<li><p><em>dbid:</em>ID database della tabella che contiene il record appena eliminato.</p></li>
<li><p><em>tableid:</em>cursore posizionato su una voce di indice associata al record appena eliminato.</p></li>
<li><p><em>pvArg1:</em> <strong>NULL</strong></p></li>
<li><p><em>pvArg2:</em> <strong>NULL</strong></p></li>
<li><p><em>pvContext:</em>puntatore di contesto passato <a href="gg269175(v=exchg.10).md">a JetRegisterCallback</a> o <strong>NULL.</strong></p></li>
<li><p><em>ulUnused</em>: <strong>NULL</strong></p></li>
</ul>
<p>Se un errore viene restituito dal callback, verrà ignorato.</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbtypUserDefinedDefaultValue<br />
0x00000080</p></td>
<td><p>Questo callback si verifica quando il motore deve recuperare il valore predefinito definito dall'utente di una colonna dall'applicazione. Questo callback è essenzialmente un'implementazione limitata di <a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a> valutata dall'applicazione. È possibile restituire un massimo di un valore di colonna per un valore predefinito definito dall'utente.</p>
<p>Il puntatore a funzione per questo motivo di callback viene passato a <a href="gg294122(v=exchg.10).md">JetAddColumn</a> tramite una struttura <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> o a <a href="gg269343(v=exchg.10).md">JetCreateTableColumnIndex</a> tramite una struttura <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> in una struttura <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> in una <a href="gg294146(v=exchg.10).md">struttura JET_TABLECREATE.</a></p>
<p>I parametri di callback avranno i valori seguenti:</p>
<ul>
<li><p><em>sesid:</em>sessione che calcola il valore predefinito definito dall'utente</p></li>
<li><p><em>dbid:</em>ID database della tabella che contiene il valore predefinito definito dall'utente</p></li>
<li><p><em>tableid:</em>cursore posizionato sul record per il quale viene recuperato il valore predefinito definito dall'utente</p></li>
<li><p><em>pvArg1:</em>buffer di output per il valore predefinito definito dall'utente</p></li>
<li><p><em>pvArg2:</em>nell'input, si tratta delle dimensioni del buffer di output. Nell'output, si tratta delle dimensioni effettive del valore predefinito definito dall'utente. in entrambi i casi, la dimensione è un intero senza segno a 32 bit.</p></li>
<li><p><em>pvContext:</em>puntatore a un buffer contenente i dati utente specificati nella <a href="gg269200(v=exchg.10).md">struttura JET_USERDEFINEDDEFAULT</a> quando è stata creata la colonna o NULL se non è stato specificato alcun contesto.</p></li>
<li><p><em>ulUnused:</em>ID della colonna per cui viene recuperato il valore predefinito definito dall'utente.</p></li>
</ul>
<p>Se viene restituito un errore dal callback, l'operazione che ha origine il callback avrà esito negativo con tale errore.</p>
<p>Se JET_wrnBufferTruncated restituito dal callback, l'operazione continuerà, ma l'intero valore non verrà recuperato durante il callback.</p>
<p>Se JET_wrnColumnNull restituito dal callback, l'operazione continuerà, ma il valore predefinito definito dall'utente per la colonna è NULL.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbtypOnlineDefragCompleted<br />
0x00000100</p></td>
<td><p>Questo callback si verifica quando la deframmentazione online di un database avviato da <a href="gg269317(v=exchg.10).md">JetDefragment</a> viene arrestata a causa del completamento del processo o del limite di tempo raggiunto.</p>
<p>Il puntatore a funzione per questo motivo di callback viene passato <a href="gg269317(v=exchg.10).md">a JetDefragment</a>. Per altre informazioni, vedere <a href="gg269317(v=exchg.10).md">JetDefragment.</a></p>
<p>I parametri di callback avranno i valori seguenti:</p>
<ul>
<li><p><em>sesid:</em>sessione usata per eseguire la deframmentazione online per il database o JET_sesidNil per un file di streaming.</p></li>
<li><p><em>dbid:</em>ID del database da deframmentare o JET_dbidNil per un file di streaming.</p></li>
<li><p><em>tableid</em>: JET_tableidNil</p></li>
<li><p><em>pvArg1:</em> <strong>NULL</strong></p></li>
<li><p><em>pvArg2:</em> <strong>NULL</strong></p></li>
<li><p><em>pvContext:</em> <strong>NULL</strong></p></li>
<li><p><em>ulUnused:</em> <strong>NULL</strong></p></li>
</ul>
<p>Se viene restituito un errore dal callback, verrà ignorato.</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbtypFreeCursorLS<br />
0x00000200</p></td>
<td><p>Questo callback si verifica quando l'applicazione deve pulire l'handle di contesto per l'Archiviazione locale associato a un cursore rilasciato dal motore di database. Per altre informazioni, vedere <a href="gg269243(v=exchg.10).md">JetSetLS.</a></p>
<p>Il puntatore a funzione per questo motivo di callback viene configurato tramite <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> <a href="gg269310(v=exchg.10).md">con JET_paramRuntimeCallback</a>.</p>
<p>I parametri di callback avranno i valori seguenti:</p>
<ul>
<li><p><em>sesid</em>: JET_sesidNil</p></li>
<li><p><em>dbid</em>: JET_dbidNil</p></li>
<li><p><em>tableid</em>: JET_tableidNil</p></li>
<li><p><em>pvArg1:</em>handle di contesto impostato con <a href="gg269243(v=exchg.10).md">JetSetLS</a></p></li>
<li><p><em>pvArg2:</em> <strong>NULL</strong></p></li>
<li><p><em>pvContext:</em> <strong>NULL</strong></p></li>
<li><p><em>ulUnused:</em> <strong>NULL</strong></p></li>
</ul>
<p>Se viene restituito un errore dal callback, verrà ignorato.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbtypFreeTableLS<br />
0x00000400</p></td>
<td><p>Questo callback si verificherà in seguito alla necessità per l'applicazione di pulire l'handle di contesto per l'Archiviazione locale associato a una tabella rilasciata dal motore di database. Per altre informazioni, vedere <a href="gg269243(v=exchg.10).md">JetSetLS.</a></p>
<p>Il puntatore a funzione per questo motivo di callback viene configurato tramite <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> <a href="gg269310(v=exchg.10).md">con JET_paramRuntimeCallback</a>.</p>
<p>I parametri di callback avranno i valori seguenti:</p>
<ul>
<li><p><em>sesid</em>: JET_sesidNil</p></li>
<li><p><em>dbid</em>: JET_dbidNil</p></li>
<li><p><em>tableid</em>: JET_tableidNil</p></li>
<li><p><em>pvArg1:</em>handle di contesto impostato usando <a href="gg269243(v=exchg.10).md">JetSetLS.</a></p></li>
<li><p><em>pvArg2:</em> <strong>NULL</strong></p></li>
<li><p><em>pvContext:</em> <strong>NULL</strong></p></li>
<li><p><em>ulUnused:</em> <strong>NULL</strong></p></li>
</ul>
<p>Se viene restituito un errore dal callback, verrà ignorato.</p></td>
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
<td><p>Dichiarato in Esent.h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Vedere anche

[JET_CALLBACK](./jet-callback-callback-function.md)
