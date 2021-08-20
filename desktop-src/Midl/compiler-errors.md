---
title: Errori del compilatore
description: Elenco di messaggi di errore generati durante la compilazione MIDL.
ms.assetid: 492eacdd-6bd1-49df-9112-3765f6c05f34
keywords:
- errori MIDL, errori del compilatore
topic_type:
- apiref
api_name:
- Compiler Errors
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 56b610025d3012446daa7938e2f37c2efcf6c2ddb7edd2ee545db0a179953fad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067453"
---
# <a name="compiler-errors"></a>Errori del compilatore

Durante la compilazione MIDL vengono generati i messaggi di errore seguenti:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Codice restituito</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="MIDL2000"></span><span id="midl2000"></span><dl> <dt><strong>MIDL2000</strong></dt> </dl></td>
<td><dl> <dt><span id="must_specify__c_ext_for_abstract_declarators"></span><span id="MUST_SPECIFY__C_EXT_FOR_ABSTRACT_DECLARATORS"></span>deve specificare /c_ext per i dichiaratori astratti</dt> <dd> I dichiaratori astratti rappresentano un'estensione Microsoft per RPC e non sono definiti nella RPC DCE. Pertanto, se il file include dichiaratori astratti, non è possibile eseguire la compilazione con l'opzione <a href="-osf.md"><strong>/osf,</strong></a> che impone una rigida compatibilità DCE. MIDL 3.0 e versioni successive usano <a href="-c-ext.md"><strong>l'opzione /c_ext</strong></a> come impostazione predefinita. <strong>L'opzione /osf</strong> disattiva l'opzione <strong>/c_ext</strong> . Per informazioni sui dichiaratori astratti, vedere <a href="/windows/desktop/Rpc/the-acf-body">Corpo ACF.</a><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2001"></span><span id="midl2001"></span><dl> <dt><strong>MIDL2001</strong></dt> </dl></td>
<td><dl> <dt><span id="instantiation_of_data_is_illegal__you_must_use__extern__or__static_"></span><span id="INSTANTIATION_OF_DATA_IS_ILLEGAL__YOU_MUST_USE__EXTERN__OR__STATIC_"></span>la creazione di un'istanza dei dati non è valida. è necessario usare &quot; extern &quot; o &quot; static&quot;</dt> <dd> La dichiarazione e l'inizializzazione nel file IDL non sono compatibili con RPC DCE. Questa funzionalità è un'estensione Microsoft che non è disponibile quando si esegue la compilazione in modalità DCE-compatibility (<a href="-osf.md"><strong>/osf</strong></a>).<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2002"></span><span id="midl2002"></span><dl> <dt><strong>MIDL2002</strong></dt> </dl></td>
<td><dl> <dt><span id="compiler_stack_overflow"></span><span id="COMPILER_STACK_OVERFLOW"></span>overflow dello stack del compilatore</dt> <dd> Il compilatore ha esaurito lo spazio dello stack durante l'elaborazione del file IDL. Questo problema può verificarsi quando il compilatore elabora una dichiarazione o un'espressione complessa. Per risolvere il problema, semplificare la dichiarazione o l'espressione complessa.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2003"></span><span id="midl2003"></span><dl> <dt><strong>MIDL2003</strong></dt> </dl></td>
<td><dl> <dt><span id="redefinition"></span><span id="REDEFINITION"></span>Ridefinizione</dt> <dd> Questo messaggio di errore può essere visualizzato nelle circostanze seguenti: un tipo è stato ridefinito; Un prototipo di procedura è stato ridefinito; esiste già un membro di una struttura o di un'unione con lo stesso nome. Nel prototipo esiste già un parametro con lo stesso nome.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2004"></span><span id="midl2004"></span><dl> <dt><strong>MIDL2004</strong></dt> </dl></td>
<td><dl> <dt><span id="_auto_handle__binding_will_be_used"></span><span id="_AUTO_HANDLE__BINDING_WILL_BE_USED"></span>[auto_handle] verrà usata l'associazione</dt> <dd> Nessun tipo di handle è stato definito come tipo di handle predefinito. Il compilatore presuppone che verrà usato un handle automatico come handle di associazione per la procedura specificata.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2005"></span><span id="midl2005"></span><dl> <dt><strong>MIDL2005</strong></dt> </dl></td>
<td><dl> <dt><span id="out_of_memory"></span><span id="OUT_OF_MEMORY"></span>memoria insufficiente</dt> <dd> Memoria insufficiente del compilatore durante la compilazione. Ridurre le dimensioni o la complessità del file IDL o allocare altra memoria al processo.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2006"></span><span id="midl2006"></span><dl> <dt><strong>MIDL2006</strong></dt> </dl></td>
<td><dl> <dt><span id="recursive_definition"></span><span id="RECURSIVE_DEFINITION"></span>definizione ricorsiva</dt> <dd> Una struttura o un'unione è stata definita in modo ricorsivo. Questo errore può verificarsi quando non viene specificata una specifica del puntatore in una definizione di struttura annidata.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2007"></span><span id="midl2007"></span><dl> <dt><strong>MIDL2007</strong></dt> </dl></td>
<td><dl> <dt><span id="import_ignored__file_already_imported"></span><span id="IMPORT_IGNORED__FILE_ALREADY_IMPORTED"></span>importazione ignorata; file già importato</dt> <dd> L'importazione di un file IDL è un'operazione idempotente. Includerlo più di una volta non ha alcun effetto. Tutte le operazioni di importazione, ad esempio la prima, vengono ignorate.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2008"></span><span id="midl2008"></span><dl> <dt><strong>MIDL2008</strong></dt> </dl></td>
<td><dl> <dt><span id="sparse_enums_require__c_ext_or__ms_ext"></span><span id="SPARSE_ENUMS_REQUIRE__C_EXT_OR__MS_EXT"></span>Le enumerazioni sparse richiedono /c_ext o /ms_ext</dt> <dd> L'assegnazione di valori alle costanti di enumerazione non è compatibile con RPC DCE. Se si desidera utilizzare le estensioni Microsoft a MIDL che consentono l'assegnazione di valori alle costanti di enumerazione, non è possibile eseguire la compilazione con l'opzione <a href="-osf.md"><strong>/osf,</strong></a> che impone la rigida compatibilità DCE. MIDL 3.0 e versioni successive usano le opzioni <a href="-c-ext.md"><strong>/c_ext</strong></a> <a href="-ms-ext.md"><strong>e /ms_ext</strong></a> come impostazione predefinita. <strong>L'opzione /osf</strong> disattiva queste opzioni di estensione.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2009"></span><span id="midl2009"></span><dl> <dt><strong>MIDL2009</strong></dt> </dl></td>
<td><dl> <dt><span id="undefined_symbol"></span><span id="UNDEFINED_SYMBOL"></span>simbolo non definito</dt> <dd> In un'espressione è stato usato un simbolo non definito. Questo errore può verificarsi quando si usa un valore enumerato non definito.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2010"></span><span id="midl2010"></span><dl> <dt><strong>MIDL2010</strong></dt> </dl></td>
<td><dl> <dt><span id="type_used_in_ACF_file_not_defined_in_IDL_file"></span><span id="type_used_in_acf_file_not_defined_in_idl_file"></span><span id="TYPE_USED_IN_ACF_FILE_NOT_DEFINED_IN_IDL_FILE"></span>Tipo usato nel file ACF non definito nel file IDL</dt> <dd> Viene usato un tipo non definito.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2011"></span><span id="midl2011"></span><dl> <dt><strong>MIDL2011</strong></dt> </dl></td>
<td><dl> <dt><span id="unresolved_type_declaration"></span><span id="UNRESOLVED_TYPE_DECLARATION"></span>dichiarazione di tipo non risolta</dt> <dd> Il tipo indicato nel campo delle informazioni aggiuntive sugli errori non è stato definito altrove nel file IDL.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2012"></span><span id="midl2012"></span><dl> <dt><strong>MIDL2012</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of_wide-character_constants_requires__ms_ext_or__c_ext"></span><span id="USE_OF_WIDE-CHARACTER_CONSTANTS_REQUIRES__MS_EXT_OR__C_EXT"></span>L'uso di costanti a caratteri wide richiede /ms_ext o /c_ext</dt> <dd> Le costanti carattere wide sono un'estensione Microsoft di DCE IDL. Per usare il tipo di dati <a href="wchar-t.md"><strong>wchar_t</strong></a>, non è possibile compilare con l'opzione <a href="-osf.md"><strong>/osf,</strong></a> che esegue l'override delle opzioni predefinite del compilatore MIDL <a href="-ms-ext.md"><strong>/ms_ext</strong></a> e <a href="-c-ext.md"><strong>/c_ext</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2013"></span><span id="midl2013"></span><dl> <dt><strong>MIDL2013</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of_wide_character_strings_requires__ms_ext_or__c_ext"></span><span id="USE_OF_WIDE_CHARACTER_STRINGS_REQUIRES__MS_EXT_OR__C_EXT"></span>L'uso di stringhe di caratteri wide richiede /ms_ext o /c_ext</dt> <dd> Le costanti stringa di caratteri wide sono un'estensione Microsoft di DCE IDL. Per usare il tipo di dati <a href="wchar-t.md"><strong>wchar_t</strong></a>, non è possibile compilare con l'opzione <a href="-osf.md"><strong>/osf,</strong></a> che esegue l'override delle opzioni predefinite del compilatore MIDL <a href="-ms-ext.md"><strong>/ms_ext</strong></a> e <a href="-c-ext.md"><strong>/c_ext</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2014"></span><span id="midl2014"></span><dl> <dt><strong>MIDL2014</strong></dt> </dl></td>
<td><dl> <dt><span id="inconsistent_redefinition_of_type_wchar_t"></span><span id="INCONSISTENT_REDEFINITION_OF_TYPE_WCHAR_T"></span>ridefinizione incoerente del tipo wchar_t</dt> <dd> Il tipo <a href="wchar-t.md"><strong>wchar_t</strong></a> è stato ridefinito come tipo che non equivale a unsigned short DOS *.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2015"></span><span id="midl2015"></span><dl> <dt><strong>MIDL2015</strong></dt> </dl></td>
<td><dl> <dt><span id="importlib_not_found"></span><span id="IMPORTLIB_NOT_FOUND"></span>importlib non trovato</dt> <dd> Il compilatore non è stato in grado di trovare la libreria dei tipi specificata dalla direttiva [ <a href="importlib.md"><strong>importlib</strong></a>]. Verificare che il percorso e il nome della libreria siano corretti.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2016"></span><span id="midl2016"></span><dl> <dt><strong>MIDL2016</strong></dt> </dl></td>
<td><dl> <dt><span id="two_library_blocks"></span><span id="TWO_LIBRARY_BLOCKS"></span>due blocchi di libreria</dt> <dd> Due blocchi di libreria (anche con nomi diversi) nello stesso file di origine non sono validi. Combinare tutti gli elementi in un unico blocco di libreria.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2017"></span><span id="midl2017"></span><dl> <dt><strong>MIDL2017</strong></dt> </dl></td>
<td><dl> <dt><span id="the_dispinterface_statement_requires_a_definition_for_IDispatch"></span><span id="the_dispinterface_statement_requires_a_definition_for_idispatch"></span><span id="THE_DISPINTERFACE_STATEMENT_REQUIRES_A_DEFINITION_FOR_IDISPATCH"></span>L'istruzione dispinterface richiede una definizione per IDispatch</dt> <dd> Questo errore si verifica in genere quando i file Stdole2.tlb o Oaidl.idl non vengono importati.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2018"></span><span id="midl2018"></span><dl> <dt><strong>MIDL2018</strong></dt> </dl></td>
<td><dl> <dt><span id="error_accessing_type_library"></span><span id="ERROR_ACCESSING_TYPE_LIBRARY"></span>errore durante l'accesso alla libreria dei tipi</dt> <dd> Il compilatore non è stato in grado di trovare la libreria dei tipi specificata. Verificare di aver specificato correttamente il percorso.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2019"></span><span id="midl2019"></span><dl> <dt><strong>MIDL2019</strong></dt> </dl></td>
<td><dl> <dt><span id="error_accessing_type_info"></span><span id="ERROR_ACCESSING_TYPE_INFO"></span>errore durante l'accesso alle informazioni sul tipo</dt> <dd> La libreria dei tipi importata è danneggiata, non valida o costruita solo parzialmente.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2020"></span><span id="midl2020"></span><dl> <dt><strong>MIDL2020</strong></dt> </dl></td>
<td><dl> <dt><span id="error_generating_type_library"></span><span id="ERROR_GENERATING_TYPE_LIBRARY"></span>errore durante la generazione della libreria dei tipi</dt> <dd> Non è stato possibile generare la libreria dei tipi. Una possibile causa di questo errore è la specifica di un percorso del file IDL di lunghezza superiore a 126 caratteri. Oleaut32.dll non supporta nomi di percorso più lunghi di 126 caratteri.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2021"></span><span id="midl2021"></span><dl> <dt><strong>MIDL2021</strong></dt> </dl></td>
<td><dl> <dt><span id="duplicate_id"></span><span id="DUPLICATE_ID"></span>ID duplicato</dt> <dd> Le applicazioni usano <a href="id.md"><strong>l'istruzione id</strong></a> nei file IDL per specificare un DISPID per le funzioni membro. Le funzioni membro possono essere proprietà o metodi di interfacce o interfacce dispatch. Questo errore indica che il file IDL specifica lo stesso numero di identificatore per due metodi o proprietà.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2022"></span><span id="midl2022"></span><dl> <dt><strong>MIDL2022</strong></dt> </dl></td>
<td><dl> <dt><span id="illegal_or_missing_value_for_entry_attribute"></span><span id="ILLEGAL_OR_MISSING_VALUE_FOR_ENTRY_ATTRIBUTE"></span>valore non valido o mancante per l'attributo entry</dt> <dd> L'argomento per l'attributo entry può essere una stringa che specifica un punto di ingresso denominato o un numero ordinale che definisce il punto di ingresso. Questo argomento è mancante o contiene un valore non valido.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2023"></span><span id="midl2023"></span><dl> <dt><strong>MIDL2023</strong></dt> </dl></td>
<td><dl> <dt><span id="error_recovery_assumes"></span><span id="ERROR_RECOVERY_ASSUMES"></span>il ripristino degli errori presuppone</dt> <dd> Il compilatore MIDL ha rilevato caratteri non validi nel file IDL.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2024"></span><span id="midl2024"></span><dl> <dt><strong>MIDL2024</strong></dt> </dl></td>
<td><dl> <dt><span id="error_recovery_discards"></span><span id="ERROR_RECOVERY_DISCARDS"></span>eliminazione del ripristino degli errori</dt> <dd> Il compilatore MIDL ha rilevato caratteri non validi nel file IDL. Verranno ignorati i caratteri non validi.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2025"></span><span id="midl2025"></span><dl> <dt><strong>MIDL2025</strong></dt> </dl></td>
<td><dl> <dt><span id="syntax_error"></span><span id="SYNTAX_ERROR"></span>Errore di sintassi</dt> <dd> Il compilatore ha rilevato un errore di sintassi nella riga specificata.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2026"></span><span id="midl2026"></span><dl> <dt><strong>MIDL2026</strong></dt> </dl></td>
<td><dl> <dt><span id="cannot_recover_from_earlier_syntax_errors__aborting_compilation"></span><span id="CANNOT_RECOVER_FROM_EARLIER_SYNTAX_ERRORS__ABORTING_COMPILATION"></span>non è in grado di eseguire il ripristino da errori di sintassi precedenti; interruzione della compilazione</dt> <dd> Il compilatore MIDL tenta automaticamente di eseguire il ripristino dagli errori di sintassi aggiungendo o rimuovendo elementi sintattici. Questo messaggio indica che, nonostante questi tentativi di ripristino, il compilatore ha rilevato troppi errori. Correggere gli errori specificati e ricompilare.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2027"></span><span id="midl2027"></span><dl> <dt><strong>MIDL2027</strong></dt> </dl></td>
<td><dl> <dt><span id="unknown_pragma_option"></span><span id="UNKNOWN_PRAGMA_OPTION"></span>opzione pragma unknown</dt> <dd> Il pragma C specificato non è supportato in MIDL. Rimuovere il pragma dal file IDL.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2028"></span><span id="midl2028"></span><dl> <dt><strong>MIDL2028</strong></dt> </dl></td>
<td><dl> <dt><span id="feature_not_implemented"></span><span id="FEATURE_NOT_IMPLEMENTED"></span>funzionalità non implementata</dt> <dd> La funzionalità MIDL, anche se parte della definizione del linguaggio, non è implementata in RPC Microsoft e non è supportata dal compilatore MIDL. Ad esempio, le funzionalità del linguaggio seguenti non vengono implementate: bitset, pipe e il tipo di carattere internazionale. La funzionalità del linguaggio non implementata viene visualizzata nel campo aggiuntivo error-information del messaggio di errore.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2029"></span><span id="midl2029"></span><dl> <dt><strong>MIDL2029</strong></dt> </dl></td>
<td><dl> <dt><span id="type_not_implemented"></span><span id="TYPE_NOT_IMPLEMENTED"></span>Tipo non implementato</dt> <dd> Il tipo di dati specificato, anche se una parola chiave MIDL valida, non viene implementato in Microsoft RPC.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2030"></span><span id="midl2030"></span><dl> <dt><strong>MIDL2030</strong></dt> </dl></td>
<td><dl> <dt><span id="non-pointer_used_in_a_dereference_operation"></span><span id="NON-POINTER_USED_IN_A_DEREFERENCE_OPERATION"></span>non puntatore usato in un'operazione di dereferenziazione</dt> <dd> Un tipo di dati che non è un puntatore è stato associato alle operazioni del puntatore. Non è possibile accedere all'oggetto tramite il non puntatore specificato.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2031"></span><span id="midl2031"></span><dl> <dt><strong>MIDL2031</strong></dt> </dl></td>
<td><dl> <dt><span id="expression_has_a_divide_by_zero"></span><span id="EXPRESSION_HAS_A_DIVIDE_BY_ZERO"></span>expression ha una divisione per zero</dt> <dd> L'espressione costante contiene la divisione per zero.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2032"></span><span id="midl2032"></span><dl> <dt><strong>MIDL2032</strong></dt> </dl></td>
<td><dl> <dt><span id="expression_uses_incompatible_types"></span><span id="EXPRESSION_USES_INCOMPATIBLE_TYPES"></span>l'espressione usa tipi incompatibili</dt> <dd> I lati sinistro e destro dell'operatore in un'espressione sono di tipi incompatibili.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2033"></span><span id="midl2033"></span><dl> <dt><strong>MIDL2033</strong></dt> </dl></td>
<td><dl> <dt><span id="nonarray_expression_uses_index_operator"></span><span id="NONARRAY_EXPRESSION_USES_INDEX_OPERATOR"></span>L'espressione non matrice usa l'operatore index</dt> <dd> L'espressione usa l'operazione di indicizzazione della matrice su un elemento di dati che non è di tipo matrice.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2034"></span><span id="midl2034"></span><dl> <dt><strong>MIDL2034</strong></dt> </dl></td>
<td><dl> <dt><span id="left-hand_side_of_expression_does_not_evaluate_to_struct_union_enum"></span><span id="LEFT-HAND_SIDE_OF_EXPRESSION_DOES_NOT_EVALUATE_TO_STRUCT_UNION_ENUM"></span>Il lato sinistro dell'espressione non restituisce struct/union/enum</dt> <dd> L'operatore di riferimento diretto o indiretto . o è stato applicato a un oggetto dati che non è &quot; &quot; una struttura, &quot; -> &quot; un'unione o un'enumerazione. Non è possibile ottenere un riferimento diretto o indiretto usando l'oggetto specificato.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2035"></span><span id="midl2035"></span><dl> <dt><strong>MIDL2035</strong></dt> </dl></td>
<td><dl> <dt><span id="constant_expression_expected"></span><span id="CONSTANT_EXPRESSION_EXPECTED"></span>Prevista espressione costante</dt> <dd> Nella sintassi era prevista un'espressione costante. Ad esempio, i limiti di matrice richiedono un'espressione costante. Il compilatore genera questo messaggio di errore quando il limite della matrice viene definito con una variabile o un simbolo non definito.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2036"></span><span id="midl2036"></span><dl> <dt><strong>MIDL2036</strong></dt> </dl></td>
<td><dl> <dt><span id="expression_cannot_be_evaluated_at_compile_time"></span><span id="EXPRESSION_CANNOT_BE_EVALUATED_AT_COMPILE_TIME"></span>L'espressione non può essere valutata in fase di compilazione</dt> <dd> Il compilatore non può valutare un'espressione in fase di compilazione.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2037"></span><span id="midl2037"></span><dl> <dt><strong>MIDL2037</strong></dt> </dl></td>
<td><dl> <dt><span id="expression_not_implemented"></span><span id="EXPRESSION_NOT_IMPLEMENTED"></span>espressione non implementata</dt> <dd> Una funzionalità supportata nelle versioni precedenti del compilatore MIDL non è supportata nella versione del compilatore fornita con Rpc Microsoft. Rimuovere l'espressione specificata.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2038"></span><span id="midl2038"></span><dl> <dt><strong>MIDL2038</strong></dt> </dl></td>
<td><dl> <dt><span id="no__pointer_default__attribute_specified__assuming__unique__for_all_unattributed_pointers"></span><span id="NO__POINTER_DEFAULT__ATTRIBUTE_SPECIFIED__ASSUMING__UNIQUE__FOR_ALL_UNATTRIBUTED_POINTERS"></span>nessun attributo [pointer_default] specificato, presupponendo che [unique] per tutti i puntatori senza attributi</dt> <dd> Il compilatore MIDL offre tre casi predefiniti diversi per i puntatori che non dispongono di attributi puntatore. Per impostazione predefinita, i parametri di funzione che sono puntatori di primo livello sono puntatori [<a href="ref.md"><strong>ref</strong></a>]. I puntatori incorporati in strutture e puntatori ad altri puntatori (non puntatori di primo livello) sono predefiniti per il tipo specificato dall'attributo [<a href="pointer-default.md"><strong>pointer_default</strong></a>]. Quando non viene<strong>fornito alcun attributo [ pointer_default</strong>] , per impostazione predefinita questi puntatori non di livello superiore sono puntatori univoci. Questo messaggio di errore indica l'ultimo caso: non viene fornito alcun attributo [<strong>pointer_default</strong>] ed è presente almeno un puntatore non di primo livello che verrà considerato come puntatore univoco. Per altre informazioni, vedere <a href="/windows/desktop/Rpc/default-pointer-types">Tipi di puntatore predefiniti</a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2039"></span><span id="midl2039"></span><dl> <dt><strong>MIDL2039</strong></dt> </dl></td>
<td><dl> <dt><span id="interface_is_not_automation_marshaling_conformant"></span><span id="INTERFACE_IS_NOT_AUTOMATION_MARSHALING_CONFORMANT"></span>L'interfaccia non è conforme al marshalling di automazione</dt> <dd> L'interfaccia non soddisfa i requisiti per un'interfaccia di automazione OLE. Verificare che l'interfaccia sia derivata da <strong>IUnknown</strong> o <strong>IDispatch</strong>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2040"></span><span id="midl2040"></span><dl> <dt><strong>MIDL2040</strong></dt> </dl></td>
<td><dl> <dt><span id="_out__only_parameter_cannot_be_a_pointer_to_an_open_structure"></span><span id="_OUT__ONLY_PARAMETER_CANNOT_BE_A_POINTER_TO_AN_OPEN_STRUCTURE"></span>[out] solo il parametro non può essere un puntatore a una struttura aperta</dt> <dd> Un parametro [<a href="out-idl.md"><strong>out</strong></a>]-only è stato usato come puntatore a una struttura, nota come struttura aperta, i cui intervalli trasmessi e le cui dimensioni vengono determinate in fase di esecuzione. Lo stub del server non conosce la quantità di spazio da allocare per una struttura aperta. Usare un puntatore a un puntatore alla struttura aperta e assicurarsi che l'applicazione server alloca spazio sufficiente.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2041"></span><span id="midl2041"></span><dl> <dt><strong>MIDL2041</strong></dt> </dl></td>
<td><dl> <dt><span id="_out__only_parameter_cannot_be_an_unsized_string"></span><span id="_OUT__ONLY_PARAMETER_CANNOT_BE_AN_UNSIZED_STRING"></span>[out] solo il parametro non può essere una stringa non disized</dt> <dd> Una matrice con l'attributo string è stata dichiarata come parametro [<a href="out-idl.md"><strong>out</strong></a>]-only senza alcuna specifica di dimensione. Lo stub del server richiede informazioni sulle dimensioni per allocare memoria per la stringa. È possibile rimuovere l'attributo stringa e aggiungere l'attributo [<a href="size-is.md"><strong>size_is</strong></a>] oppure modificare il parametro in un parametro [<strong>in, out</strong>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2042"></span><span id="midl2042"></span><dl> <dt><strong>MIDL2042</strong></dt> </dl></td>
<td><dl> <dt><span id="_out__parameter_is_not_a_pointer"></span><span id="_OUT__PARAMETER_IS_NOT_A_POINTER"></span>Il parametro [out] non è un puntatore</dt> <dd> Tutti i parametri [<a href="out-idl.md"><strong>out</strong></a>] devono essere puntatori, in base alla convenzione di chiamata per valore del linguaggio di programmazione C. Il parametro<strong>direzionale</strong>[ out ] indica che il server trasmette un valore al client. Con la convenzione di chiamata per valore, il server può trasmettere dati al client solo se l'argomento della funzione è un puntatore.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2043"></span><span id="midl2043"></span><dl> <dt><strong>MIDL2043</strong></dt> </dl></td>
<td><dl> <dt><span id="open_structure_cannot_be_a_parameter"></span><span id="OPEN_STRUCTURE_CANNOT_BE_A_PARAMETER"></span>open structure non può essere un parametro</dt> <dd> Una struttura aperta contiene una matrice conforme come ultimo elemento. Una struttura o un'unione viene troncata quando l'ultimo elemento di tale struttura o unione è una matrice conforme.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2044"></span><span id="midl2044"></span><dl> <dt><strong>MIDL2044</strong></dt> </dl></td>
<td><dl> <dt><span id="_out__context_handle_generic_handle_must_be_specified_as_a_pointer_to_that_handle_type"></span><span id="_OUT__CONTEXT_HANDLE_GENERIC_HANDLE_MUST_BE_SPECIFIED_AS_A_POINTER_TO_THAT_HANDLE_TYPE"></span>[out] handle di contesto/handle generico deve essere specificato come puntatore a tale tipo di handle</dt> <dd> Un parametro handle definito dal contesto o definito dall'utente con l'attributo direzionale [<a href="out-idl.md"><strong>out</strong></a>] deve essere un puntatore a un puntatore.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2045"></span><span id="midl2045"></span><dl> <dt><strong>MIDL2045</strong></dt> </dl></td>
<td><dl> <dt><span id="context_handle_must_not_derive_from_a_type_that_has_the__transmit_as__attribute"></span><span id="CONTEXT_HANDLE_MUST_NOT_DERIVE_FROM_A_TYPE_THAT_HAS_THE__TRANSMIT_AS__ATTRIBUTE"></span>L'handle di contesto non deve derivare da un tipo con l'attributo [transmit_as]</dt> <dd> Gli handle di contesto devono essere trasmessi come tipi di handle di contesto. Non possono essere trasmessi come altri tipi e non possono derivare da [transmit_is], [<strong>represent_as</strong>], [<strong>wire_marshal</strong>], o [<strong>user_marshal</strong>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2046"></span><span id="midl2046"></span><dl> <dt><strong>MIDL2046</strong></dt> </dl></td>
<td><dl> <dt><span id="cannot_specify_a_variable_number_of_arguments_to_a_remote_procedure"></span><span id="CANNOT_SPECIFY_A_VARIABLE_NUMBER_OF_ARGUMENTS_TO_A_REMOTE_PROCEDURE"></span>impossibile specificare un numero variabile di argomenti per una procedura remota</dt> <dd> Le chiamate di procedura remota che specificano un numero variabile di argomenti in fase di compilazione non sono compatibili con la definizione RPC DCE. Non è possibile usare un numero variabile di argomenti in Microsoft RPC.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2047"></span><span id="midl2047"></span><dl> <dt><strong>MIDL2047</strong></dt> </dl></td>
<td><dl> <dt><span id="named_parameter_cannot_be__void_"></span><span id="NAMED_PARAMETER_CANNOT_BE__VOID_"></span>il parametro denominato non può essere &quot; void&quot;</dt> <dd> Un parametro con il tipo di base <a href="void.md"><strong>void</strong></a> viene specificato con un nome.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2048"></span><span id="midl2048"></span><dl> <dt><strong>MIDL2048</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_derives_from__coclass__or__module_"></span><span id="PARAMETER_DERIVES_FROM__COCLASS__OR__MODULE_"></span>il parametro deriva dalla &quot; coclasse &quot; o dal &quot; modulo&quot;</dt> <dd> La <a href="coclass.md"><strong>coclasse</strong></a> specifica un oggetto di primo livello che contiene interfacce e interfacce dispatch. Non può essere passato come parametro.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2049"></span><span id="midl2049"></span><dl> <dt><strong>MIDL2049</strong></dt> </dl></td>
<td><dl> <dt><span id="only_the_first_parameter_can_be_a_binding_handle__you_must_specify_the__ms_ext_switch"></span><span id="ONLY_THE_FIRST_PARAMETER_CAN_BE_A_BINDING_HANDLE__YOU_MUST_SPECIFY_THE__MS_EXT_SWITCH"></span>solo il primo parametro può essere un handle di associazione. è necessario specificare l'opzione /ms_ext</dt> <dd> DCE RPC consente solo al primo parametro di essere un handle di associazione. La compilazione con l'opzione <a href="-osf.md"><strong>/osf</strong></a> disattiva l'opzione <a href="-ms-ext.md"><strong>/ms_ext</strong></a> predefinita che supporta più parametri di handle e gestisce i parametri in una posizione diversa da quella più a sinistra.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2050"></span><span id="midl2050"></span><dl> <dt><strong>MIDL2050</strong></dt> </dl></td>
<td><dl> <dt><span id="cannot_use__comm_status__on_both_a_parameter_and_a_return_type"></span><span id="CANNOT_USE__COMM_STATUS__ON_BOTH_A_PARAMETER_AND_A_RETURN_TYPE"></span>impossibile usare [comm_status] sia in un parametro che in un tipo restituito</dt> <dd> Sia la routine che uno dei relativi parametri hanno<a href="comm-status.md"><strong>l'attributo</strong></a>[ comm_status ]. <strong>L'attributo [ comm_status</strong>] specifica che un solo oggetto dati alla volta può essere di tipo <a href="error-status-t.md"><strong>error_status_t</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2051"></span><span id="midl2051"></span><dl> <dt><strong>MIDL2051</strong></dt> </dl></td>
<td><dl> <dt><span id="__local__attribute_on_a_procedure_requires__ms_ext"></span><span id="__LOCAL__ATTRIBUTE_ON_A_PROCEDURE_REQUIRES__MS_EXT"></span> L'attributo [local] in una routine richiede /ms_ext</dt> <dd> <a href="local.md"><strong>L'attributo</strong></a>[ local ] è un'estensione Microsoft per DCE IDL. Per usare questo attributo in una funzione, non è possibile eseguire la compilazione con <a href="-osf.md"><strong>l'opzione /osf.</strong></a> <strong>L'opzione /osf</strong> esegue l'override delle opzioni predefinite del compilatore MIDL <a href="-ms-ext.md"><strong>/ms_ext</strong></a> <a href="-c-ext.md"><strong>e /c_ext</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2052"></span><span id="midl2052"></span><dl> <dt><strong>MIDL2052</strong></dt> </dl></td>
<td><dl> <dt><span id="property_attributes_may_only_be_used_with_procedures"></span><span id="PROPERTY_ATTRIBUTES_MAY_ONLY_BE_USED_WITH_PROCEDURES"></span>Gli attributi di proprietà possono essere usati solo con le routine</dt> <dd> Uso non corretto di un attributo [<a href="propget.md"><strong>propget</strong></a>], [<a href="propput.md"><strong>propput</strong></a>] o [<a href="propputref.md"><strong>propputref</strong></a>]. Assicurarsi di aver digitato correttamente il nome della funzione della proprietà e che la proprietà e la funzione hanno lo stesso nome.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2053"></span><span id="midl2053"></span><dl> <dt><strong>MIDL2053</strong></dt> </dl></td>
<td><dl> <dt><span id="a_procedure_may_not_have_more_than_one_property_attribute"></span><span id="A_PROCEDURE_MAY_NOT_HAVE_MORE_THAN_ONE_PROPERTY_ATTRIBUTE"></span>una routine non può avere più di un attributo di proprietà</dt> <dd> Al massimo, è possibile specificare solo uno degli attributi [<a href="propget.md"><strong>propget</strong></a>], [<a href="propput.md"><strong>propput</strong></a>], o [<a href="propputref.md"><strong>propputref</strong></a>] per una funzione.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2054"></span><span id="midl2054"></span><dl> <dt><strong>MIDL2054</strong></dt> </dl></td>
<td><dl> <dt><span id="the_procedure_has_an_illegal_combination_of_operation_attributes"></span><span id="THE_PROCEDURE_HAS_AN_ILLEGAL_COMBINATION_OF_OPERATION_ATTRIBUTES"></span>la procedura ha una combinazione non valida di attributi dell'operazione</dt> <dd> Alcuni attributi non possono essere usati in connessione con altri attributi. Controllare le informazioni di riferimento sul linguaggio MIDL per i requisiti e la sintassi esatti degli attributi usati in questa procedura.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2055"></span><span id="midl2055"></span><dl> <dt><strong>MIDL2055</strong></dt> </dl></td>
<td><dl> <dt><span id="field_deriving_from_a_conformant_array_must_be_the_last_member_of_the_structure"></span><span id="FIELD_DERIVING_FROM_A_CONFORMANT_ARRAY_MUST_BE_THE_LAST_MEMBER_OF_THE_STRUCTURE"></span>il campo derivante da una matrice conforme deve essere l'ultimo membro della struttura</dt> <dd> La struttura contiene una matrice conforme che non è l'ultimo elemento della struttura . La matrice conforme deve essere visualizzata come ultimo elemento della struttura.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2056"></span><span id="midl2056"></span><dl> <dt><strong>MIDL2056</strong></dt> </dl></td>
<td><dl> <dt><span id="duplicate__case__label"></span><span id="DUPLICATE__CASE__LABEL"></span>etichetta [case] duplicata</dt> <dd> È stata specificata un'etichetta case duplicata. Viene visualizzata l'etichetta duplicata.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2057"></span><span id="midl2057"></span><dl> <dt><strong>MIDL2057</strong></dt> </dl></td>
<td><dl> <dt><span id="no__default__case_specified_for_discriminated_union"></span><span id="NO__DEFAULT__CASE_SPECIFIED_FOR_DISCRIMINATED_UNION"></span>nessun case [predefinito] specificato per l'unione discriminata</dt> <dd> È stata specificata un'unione discriminata senza un caso predefinito.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2058"></span><span id="midl2058"></span><dl> <dt><strong>MIDL2058</strong></dt> </dl></td>
<td><dl> <dt><span id="attribute_expression_cannot_be_resolved"></span><span id="ATTRIBUTE_EXPRESSION_CANNOT_BE_RESOLVED"></span>Impossibile risolvere l'espressione dell'attributo</dt> <dd> L'espressione associata all'attributo non può essere risolta. Questo errore si verifica in genere quando una variabile visualizzata nell'espressione non è definita. Ad esempio, l'errore può verificarsi quando la variabile <em>s</em> non è definita e viene usata dall'attributo [<a href="size-is.md"><strong>size_is</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2059"></span><span id="midl2059"></span><dl> <dt><strong>MIDL2059</strong></dt> </dl></td>
<td><dl> <dt><span id="attribute_expression_must_be_of_integral_type__no_support_for_64-bit_expressions"></span><span id="ATTRIBUTE_EXPRESSION_MUST_BE_OF_INTEGRAL_TYPE__NO_SUPPORT_FOR_64-BIT_EXPRESSIONS"></span>L'espressione dell'attributo deve essere di tipo integrale, non è supportato per le espressioni a 64 bit</dt> <dd> La variabile o l'espressione di attributo specificata deve essere un tipo integrale. Questo errore si verifica quando il tipo attribute-expression non viene risolto in un integer.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2060"></span><span id="midl2060"></span><dl> <dt><strong>MIDL2060</strong></dt> </dl></td>
<td><dl> <dt><span id="_byte_count__requires__ms_ext"></span><span id="_BYTE_COUNT__REQUIRES__MS_EXT"></span>[byte_count] richiede /ms_ext</dt> <dd> <a href="byte-count.md"><strong>L'attributo</strong></a>[ byte_count ] è un'estensione Microsoft per DCE IDL. Per usare questo attributo non è possibile eseguire la compilazione con l'opzione <a href="-osf.md"><strong>/osf,</strong></a> che esegue l'override delle opzioni predefinite del compilatore MIDL <a href="-ms-ext.md"><strong>/ms_ext</strong></a> <a href="-c-ext.md"><strong>e /c_ext</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2061"></span><span id="midl2061"></span><dl> <dt><strong>MIDL2061</strong></dt> </dl></td>
<td><dl> <dt><span id="_byte_count__can_be_applied_only_to_out_parameters_of_pointer_type"></span><span id="_BYTE_COUNT__CAN_BE_APPLIED_ONLY_TO_OUT_PARAMETERS_OF_POINTER_TYPE"></span>[byte_count] può essere applicato solo ai parametri out del tipo di puntatore</dt> <dd> <a href="byte-count.md"><strong>L'attributo</strong></a>[ byte_count ] può essere applicato solo ai parametri [<a href="out-idl.md"><strong>out</strong></a>] e tutti i parametri [<strong>out</strong>] devono essere tipi puntatore.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2062"></span><span id="midl2062"></span><dl> <dt><strong>MIDL2062</strong></dt> </dl></td>
<td><dl> <dt><span id="_byte_count__cannot_be_specified_on_a_pointer_to_a_conformant_array_or_structure"></span><span id="_BYTE_COUNT__CANNOT_BE_SPECIFIED_ON_A_POINTER_TO_A_CONFORMANT_ARRAY_OR_STRUCTURE"></span>[byte_count] non può essere specificato su un puntatore a una matrice o a una struttura conforme</dt> <dd> <a href="byte-count.md"><strong>L'attributo</strong></a>[ byte_count ] non può essere applicato a una matrice o a una struttura conforme.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2063"></span><span id="midl2063"></span><dl> <dt><strong>MIDL2063</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_specifying_the_byte_count_is_not__in__only_or_byte_count_parameter_is_not__out__only"></span><span id="PARAMETER_SPECIFYING_THE_BYTE_COUNT_IS_NOT__IN__ONLY_OR_BYTE_COUNT_PARAMETER_IS_NOT__OUT__ONLY"></span>il parametro che specifica il numero di byte non è solo [in] o il parametro byte count non è solo [out]</dt> <dd> Il valore associato a [<a href="byte-count.md"><strong>byte_count</strong></a>] deve essere trasmesso dal client al server. deve essere un parametro [<a href="in.md"><strong>in</strong></a>]. Il parametro<strong>[ byte_count</strong>] non deve essere un parametro [<strong>in, out</strong>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2064"></span><span id="midl2064"></span><dl> <dt><strong>MIDL2064</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_specifying_the_byte_count_is_not_an_integral_type"></span><span id="PARAMETER_SPECIFYING_THE_BYTE_COUNT_IS_NOT_AN_INTEGRAL_TYPE"></span>il parametro che specifica il numero di byte non è un tipo integrale</dt> <dd> Il valore associato al conteggio dei byte deve essere di tipo <a href="int.md"><strong>integer int</strong></a>, <a href="small.md"><strong>small</strong></a>, <a href="short.md"><strong>short</strong></a>o <a href="long.md"><strong>long</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2065"></span><span id="midl2065"></span><dl> <dt><strong>MIDL2065</strong></dt> </dl></td>
<td><dl> <dt><span id="_byte_count__cannot_be_specified_on_a_parameter_with_size_attributes"></span><span id="_BYTE_COUNT__CANNOT_BE_SPECIFIED_ON_A_PARAMETER_WITH_SIZE_ATTRIBUTES"></span>[byte_count] non può essere specificato in un parametro con attributi di dimensione</dt> <dd> <a href="byte-count.md"><strong>L'attributo</strong></a>[ byte_count ] non può essere usato con altri attributi di dimensione, ad esempio [<a href="size-is.md"><strong>size_is</strong></a>] o [<a href="length-is.md"><strong>length_is</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2066"></span><span id="midl2066"></span><dl> <dt><strong>MIDL2066</strong></dt> </dl></td>
<td><dl> <dt><span id="_case__expression_is_not_constant"></span><span id="_CASE__EXPRESSION_IS_NOT_CONSTANT"></span>L'espressione [case] non è costante</dt> <dd> L'espressione specificata per l'etichetta case non è una costante.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2067"></span><span id="midl2067"></span><dl> <dt><strong>MIDL2067</strong></dt> </dl></td>
<td><dl> <dt><span id="_case__expression_is_not_of_integral_type"></span><span id="_CASE__EXPRESSION_IS_NOT_OF_INTEGRAL_TYPE"></span>[case] expression non è di tipo integrale</dt> <dd> L'espressione specificata per l'etichetta case non è di tipo Integer.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2068"></span><span id="midl2068"></span><dl> <dt><strong>MIDL2068</strong></dt> </dl></td>
<td><dl> <dt><span id="specifying__context_handle__on_a_type_other_than_void___requires__ms_ext"></span><span id="SPECIFYING__CONTEXT_HANDLE__ON_A_TYPE_OTHER_THAN_VOID___REQUIRES__MS_EXT"></span>se si specifica [context_handle] in un tipo diverso da void * è necessario /ms_ext</dt> <dd> Per la compatibilità DCE-RPC, l'handle di contesto deve essere un puntatore di tipo <strong>void *</strong>. Se si desidera associare gli handle di contesto a tipi diversi da <strong>void *,</strong>non usare l'opzione <a href="-osf.md"><strong>/osf</strong></a>del compilatore MIDL , che esegue l'override dell'opzione predefinita /ms_ext del <a href="-ms-ext.md"><strong>compilatore MIDL.</strong></a><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2069"></span><span id="midl2069"></span><dl> <dt><strong>MIDL2069</strong></dt> </dl></td>
<td><dl> <dt><span id="cannot_specify_more_than_one_parameter_with_each_of_comm_status_fault_status"></span><span id="CANNOT_SPECIFY_MORE_THAN_ONE_PARAMETER_WITH_EACH_OF_COMM_STATUS_FAULT_STATUS"></span>non può specificare più di un parametro con ogni comm_status/fault_status</dt> <dd> Una routine può avere un solo parametro con<a href="comm-status.md"><strong>l'attributo</strong></a>[ comm_status ]. Può avere al massimo un parametro con<a href="fault-status.md"><strong>l'attributo</strong></a>[ fault_status ].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2070"></span><span id="midl2070"></span><dl> <dt><strong>MIDL2070</strong></dt> </dl></td>
<td><dl> <dt><span id="comm_status_fault_status_parameter_must_be_an__out__only_pointer_parameter"></span><span id="COMM_STATUS_FAULT_STATUS_PARAMETER_MUST_BE_AN__OUT__ONLY_POINTER_PARAMETER"></span>comm_status/fault_status parametro deve essere un parametro puntatore solo [out]</dt> <dd> I tipi di codice di errore [<a href="comm-status.md"><strong>comm_status</strong></a>] e [<a href="fault-status.md"><strong>fault_status</strong></a>] vengono trasmessi dal server al client e pertanto devono essere specificati come parametro [<a href="out-idl.md"><strong>out</strong></a>]. A causa dei vincoli nel linguaggio di programmazione C, tutti i parametri [<strong>out</strong>] devono essere puntatori.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2071"></span><span id="midl2071"></span><dl> <dt><strong>MIDL2071</strong></dt> </dl></td>
<td><dl> <dt><span id="endpoint_syntax_error"></span><span id="ENDPOINT_SYNTAX_ERROR"></span>Errore di sintassi dell'endpoint</dt> <dd> La sintassi dell'endpoint non è corretta.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2072"></span><span id="midl2072"></span><dl> <dt><strong>MIDL2072</strong></dt> </dl></td>
<td><dl> <dt><span id="inapplicable_attribute"></span><span id="INAPPLICABLE_ATTRIBUTE"></span>attributo inapplicable</dt> <dd> L'attributo specificato non può essere applicato in questo costrutto. Ad esempio, l'attributo string si applica alle matrici <a href="char-idl.md"><strong>char</strong></a> o ai puntatori <strong>char</strong> e non può essere applicato a una struttura costituita da <a href="short.md"><strong>due numeri interi</strong></a> brevi: <br/>
<pre class="syntax" data-space="preserve"><code>typedef [string] struct moo 
{
    short x;
    short y;
};</code></pre>
</dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2073"></span><span id="midl2073"></span><dl> <dt><strong>MIDL2073</strong></dt> </dl></td>
<td><dl> <dt><span id="_allocate__requires__ms_ext"></span><span id="_ALLOCATE__REQUIRES__MS_EXT"></span>[allocate] richiede /ms_ext</dt> <dd> <a href="allocate.md"><strong>L'attributo allocate</strong></a> rappresenta un'estensione Microsoft non definita come parte di RPC DCE. Per usare questo attributo, non è possibile eseguire la compilazione con l'opzione <a href="-osf.md"><strong>/osf,</strong></a> che esegue l'override dell'opzione predefinita del compilatore MIDL <a href="-ms-ext.md"><strong>/ms_ext</strong></a><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2074"></span><span id="midl2074"></span><dl> <dt><strong>MIDL2074</strong></dt> </dl></td>
<td><dl> <dt><span id="invalid__allocate__mode"></span><span id="INVALID__ALLOCATE__MODE"></span>modalità non valida [allocare]</dt> <dd> È stata specificata una modalità non valida per il costrutto di attributo [<a href="allocate.md"><strong>allocate</strong></a>]. Le quattro modalità valide sono single_node, all_nodes, on_null e sempre.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2075"></span><span id="midl2075"></span><dl> <dt><strong>MIDL2075</strong></dt> </dl></td>
<td><dl> <dt><span id="length_attributes_cannot_be_applied_with_string_attribute"></span><span id="LENGTH_ATTRIBUTES_CANNOT_BE_APPLIED_WITH_STRING_ATTRIBUTE"></span>Gli attributi di lunghezza non possono essere applicati con l'attributo stringa</dt> <dd> Quando viene usato l'attributo stringa, i file stub generati chiamano la <strong>funzione strlen</strong> per determinare la lunghezza della stringa. Non usare l'attributo length e l'attributo stringa per la stessa variabile.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2076"></span><span id="midl2076"></span><dl> <dt><strong>MIDL2076</strong></dt> </dl></td>
<td><dl> <dt><span id="_last_is__and__length_is__cannot_be_specified_at_the_same_time"></span><span id="_LAST_IS__AND__LENGTH_IS__CANNOT_BE_SPECIFIED_AT_THE_SAME_TIME"></span>[last_is] e [length_is] non possono essere specificati contemporaneamente</dt> <dd> Sia [<a href="last-is.md"><strong>last_is</strong></a>] che [<a href="length-is.md"><strong>length_is</strong></a>] sono stati specificati per la stessa matrice. Questi attributi sono correlati come segue: length = last first + 1. Poiché ogni valore può essere derivato dall'altro, non specificare entrambi.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2077"></span><span id="midl2077"></span><dl> <dt><strong>MIDL2077</strong></dt> </dl></td>
<td><dl> <dt><span id="_max_is__and__size_is__cannot_be_specified_at_the_same_time"></span><span id="_MAX_IS__AND__SIZE_IS__CANNOT_BE_SPECIFIED_AT_THE_SAME_TIME"></span>[max_is] e [size_is] non possono essere specificati contemporaneamente</dt> <dd> Sia [ <a href="max-is.md"><strong>max_is</strong></a>] che [ <a href="size-is.md"><strong>size_is</strong></a>] sono stati specificati per la stessa matrice. Questi attributi sono correlati come segue: max = size + 1. Poiché ogni valore può essere derivato dall'altro, non specificare entrambi.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2078"></span><span id="midl2078"></span><dl> <dt><strong>MIDL2078</strong></dt> </dl></td>
<td><dl> <dt><span id="no__switch_is__attribute_specified_at_use_of_union"></span><span id="NO__SWITCH_IS__ATTRIBUTE_SPECIFIED_AT_USE_OF_UNION"></span>nessun attributo [switch_is] specificato all'uso dell'unione</dt> <dd> Non è stato specificato alcun discriminante per l'unione. <a href="switch-is.md"><strong>L'attributo [ switch_is</strong></a>] indica la discriminante usata per selezionare tra i campi unione.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2079"></span><span id="midl2079"></span><dl> <dt><strong>MIDL2079</strong></dt> </dl></td>
<td><dl> <dt><span id="no__uuid__specified"></span><span id="NO__UUID__SPECIFIED"></span>nessun [uuid] specificato</dt> <dd> Per l'interfaccia non è stato specificato alcun UUID.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2080"></span><span id="midl2080"></span><dl> <dt><strong>MIDL2080</strong></dt> </dl></td>
<td><dl> <dt><span id="_uuid__ignored_on__local__interface"></span><span id="_UUID__IGNORED_ON__LOCAL__INTERFACE"></span>[uuid] ignorato nell'interfaccia [local]</dt> <dd> L'uso<a href="local.md"><strong>dell'attributo</strong></a>[ local ] su un'interfaccia oggetto fa sì che il compilatore MIDL ignori l'attributo [<a href="uuid.md"><strong>uuid</strong></a>]. Non è possibile usare entrambi gli attributi in un'interfaccia RPC.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2081"></span><span id="midl2081"></span><dl> <dt><strong>MIDL2081</strong></dt> </dl></td>
<td><dl> <dt><span id="type_mismatch_between_length_and_size_attribute_expressions"></span><span id="TYPE_MISMATCH_BETWEEN_LENGTH_AND_SIZE_ATTRIBUTE_EXPRESSIONS"></span>Mancata corrispondenza di tipo tra espressioni di attributi di lunghezza e dimensioni</dt> <dd> Le espressioni dell'attributo length e size devono essere degli stessi tipi. Ad esempio, questo avviso viene generato quando la variabile di attributo per l'espressione [<a href="size-is.md"><strong>size_is</strong></a>] è di tipo <strong>unsigned long</strong> e la variabile di attributo per l'espressione [<a href="length-is.md"><strong>length_is</strong></a>] è di tipo <a href="long.md"><strong>long</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2082"></span><span id="midl2082"></span><dl> <dt><strong>MIDL2082</strong></dt> </dl></td>
<td><dl> <dt><span id="_string__attribute_must_be_specified__byte____char___or__wchar_t__array_or_pointer"></span><span id="_STRING__ATTRIBUTE_MUST_BE_SPECIFIED__BYTE____CHAR___OR__WCHAR_T__ARRAY_OR_POINTER"></span>L'attributo [string] deve essere byte, char o &quot; &quot; &quot; wchar_t matrice &quot; o &quot; &quot; puntatore</dt> <dd> Un attributo stringa non può essere applicato a un puntatore o a una matrice il cui tipo di base non è un <a href="byte.md"><strong>byte,</strong></a> <a href="char-idl.md"><strong>char</strong></a>o <a href="struct.md"><strong>struct</strong></a> in cui i membri sono tutti di tipo <strong>byte</strong> <strong>o char.</strong><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2083"></span><span id="midl2083"></span><dl> <dt><strong>MIDL2083</strong></dt> </dl></td>
<td><dl> <dt><span id="mismatch_between_the_type_of_the__switch_is__expression_and_the_switch_type_of_the_union"></span><span id="MISMATCH_BETWEEN_THE_TYPE_OF_THE__SWITCH_IS__EXPRESSION_AND_THE_SWITCH_TYPE_OF_THE_UNION"></span>mancata corrispondenza tra il tipo dell'espressione [switch_is] e il tipo switch dell'unione</dt> <dd> Se<a href="switch-type.md"><strong>l'unione</strong></a>[ switch_type ] non viene specificata, il tipo di opzione è dello stesso tipo del campo [<a href="switch-is.md"><strong>switch_is</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2084"></span><span id="midl2084"></span><dl> <dt><strong>MIDL2084</strong></dt> </dl></td>
<td><dl> <dt><span id="_transmit_as__must_not_be_applied_to_a_type_that_derives_from_a_context_handle"></span><span id="_TRANSMIT_AS__MUST_NOT_BE_APPLIED_TO_A_TYPE_THAT_DERIVES_FROM_A_CONTEXT_HANDLE"></span>[transmit_as] non deve essere applicato a un tipo che deriva da un handle di contesto</dt> <dd> Gli handle di contesto non possono essere trasmessi come altri tipi.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2085"></span><span id="midl2085"></span><dl> <dt><strong>MIDL2085</strong></dt> </dl></td>
<td><dl> <dt><span id="_transmit_as__must_specify_a_transmissible_type"></span><span id="_TRANSMIT_AS__MUST_SPECIFY_A_TRANSMISSIBLE_TYPE"></span>[transmit_as] deve specificare un tipo trasmissibile</dt> <dd> Il tipo [<a href="transmit-as.md"><strong>transmit_as</strong></a>] specificato deriva da un tipo che non può essere trasmesso da Microsoft RPC, ad esempio <a href="void.md"><strong>void</strong></a>, <strong>void *</strong>o <a href="int.md"><strong>int</strong></a>. Usare un tipo di base RPC definito. nel caso di <strong>int</strong>, aggiungere identificatori di dimensione come <a href="small.md"><strong>small</strong></a>, <a href="short.md"><strong>short</strong></a>o <a href="long.md"><strong>long</strong></a> per qualificare <strong>int</strong>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2086"></span><span id="midl2086"></span><dl> <dt><strong>MIDL2086</strong></dt> </dl></td>
<td><dl> <dt><span id="transmitted_type_for__transmit_as__and__represent_as__must_not_be_a_pointer_or_derive_from_a_pointer"></span><span id="TRANSMITTED_TYPE_FOR__TRANSMIT_AS__AND__REPRESENT_AS__MUST_NOT_BE_A_POINTER_OR_DERIVE_FROM_A_POINTER"></span>Il tipo trasmesso per [transmit_as] e [represent_as] non deve essere un puntatore o derivare da un puntatore</dt> <dd> Il tipo trasmesso non può essere un puntatore o derivare da un puntatore.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2087"></span><span id="midl2087"></span><dl> <dt><strong>MIDL2087</strong></dt> </dl></td>
<td><dl> <dt><span id="presented_type_for__transmit_as__and__represent_as__must_not_derive_from_a_conformant_varying_array__its_pointer_equivalent__or_a_conformant_varying_structure"></span><span id="PRESENTED_TYPE_FOR__TRANSMIT_AS__AND__REPRESENT_AS__MUST_NOT_DERIVE_FROM_A_CONFORMANT_VARYING_ARRAY__ITS_POINTER_EQUIVALENT__OR_A_CONFORMANT_VARYING_STRUCTURE"></span>il tipo presentato per [transmit_as] e [represent_as] non deve derivare da una matrice conforme/variabile, dal relativo equivalente puntatore o da una struttura conforme/variabile</dt> <dd> Il tipo a cui è<a href="transmit-as.md"><strong>stato applicato [ transmit_as</strong></a>] non può derivare da una matrice o una struttura conforme (una matrice o una struttura le cui dimensioni sono determinate in fase di esecuzione).<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2088"></span><span id="midl2088"></span><dl> <dt><strong>MIDL2088</strong></dt> </dl></td>
<td><dl> <dt><span id="_uuid__format_is_incorrect"></span><span id="_UUID__FORMAT_IS_INCORRECT"></span>Il formato [uuid] non è corretto</dt> <dd> Il formato UUID non è conforme alle specifiche. L'UUID deve essere una stringa costituita da cinque sequenze di cifre esadecimali di lunghezza 8, 4, 4, 4, 4 e 12 cifre. &quot;12345678-1234-ABCD-EF01-28A49C28F17D &quot; è un UUID valido. Usare la funzione <a href="/windows/desktop/api/rpcdce/nf-rpcdce-uuidcreate"><strong>UuidCreate</strong></a> o un'utilità per generare un UUID valido.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2089"></span><span id="midl2089"></span><dl> <dt><strong>MIDL2089</strong></dt> </dl></td>
<td><dl> <dt><span id="uuid_is_not_a_hexadecimal_number"></span><span id="UUID_IS_NOT_A_HEXADECIMAL_NUMBER"></span>uuid non è un numero esadecimale</dt> <dd> L'UUID specificato per l'interfaccia contiene caratteri non validi in una rappresentazione numerica esadecimale. I caratteri da 0 a 9 e da A a F sono validi in una rappresentazione esadecimale.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2090"></span><span id="midl2090"></span><dl> <dt><strong>MIDL2090</strong></dt> </dl></td>
<td><dl> <dt><span id="optional_parameters_must_come_after_required_parameters"></span><span id="OPTIONAL_PARAMETERS_MUST_COME_AFTER_REQUIRED_PARAMETERS"></span>I parametri facoltativi devono essere specificati dopo i parametri obbligatori</dt> <dd> Per una descrizione dell'ordinamento degli elenchi di parametri, vedere [<a href="optional.md"><strong>facoltativo</strong></a>] nelle informazioni di riferimento sul linguaggio MIDL.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2091"></span><span id="midl2091"></span><dl> <dt><strong>MIDL2091</strong></dt> </dl></td>
<td><dl> <dt><span id="_dllname__required_when__entry__is_used"></span><span id="_DLLNAME__REQUIRED_WHEN__ENTRY__IS_USED"></span>[dllname] obbligatorio quando si usa [entry]</dt> <dd> Se si specifica un punto di ingresso in una DLL, è necessario specificare anche il nome di tale DLL usando l'attributo [<a href="dllname-str-.md"><strong>dllname</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2092"></span><span id="midl2092"></span><dl> <dt><strong>MIDL2092</strong></dt> </dl></td>
<td><dl> <dt><span id="_bindable__is_invalid_without__propget____propput___or__propputref_"></span><span id="_BINDABLE__IS_INVALID_WITHOUT__PROPGET____PROPPUT___OR__PROPPUTREF_"></span>[bindable] non è valido senza [propget], [propput] o [propputref]</dt> <dd> L'attributo [<a href="bindable.md"><strong>associabile</strong></a>] è valido solo per una proprietà, pertanto è necessario specificare anche una delle funzioni di accesso alle proprietà o di impostazione delle proprietà.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2093"></span><span id="midl2093"></span><dl> <dt><strong>MIDL2093</strong></dt> </dl></td>
<td><dl> <dt><span id="procedures_with__propput__or__propputref__must_have_at_least_one_parameter"></span><span id="PROCEDURES_WITH__PROPPUT__OR__PROPPUTREF__MUST_HAVE_AT_LEAST_ONE_PARAMETER"></span>Le routine con [propput] o [propputref] devono avere almeno un parametro</dt> <dd> Una routine [<a href="propput.md"><strong>propput</strong></a>] o [ <a href="propputref.md"><strong>propputref</strong></a>] deve avere almeno un parametro [<a href="in.md"><strong>in</strong></a>] con la proprietà da impostare. Una routine [<a href="propget.md"><strong>propget</strong></a>] deve avere almeno un parametro [<a href="out-idl.md"><strong>out</strong></a>, <a href="retval.md"><strong>retval</strong></a>] per ricevere la proprietà o il riferimento.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2094"></span><span id="midl2094"></span><dl> <dt><strong>MIDL2094</strong></dt> </dl></td>
<td><dl> <dt><span id="_id__attribute_is_required"></span><span id="_ID__ATTRIBUTE_IS_REQUIRED"></span>L'attributo [id] è obbligatorio</dt> <dd> Questa funzione membro, a causa della sintassi <a href="dispinterface.md"><strong>dell'interfaccia dispatch</strong></a> usata, richiede un DISPID, specificato usando l'attributo [ <a href="id.md"><strong>id</strong></a>]. Quando si specifica <strong>un'interfaccia dispatch</strong> usando proprietà e metodi, è necessario specificare un DISPID per ogni proprietà e metodo.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2095"></span><span id="midl2095"></span><dl> <dt><strong>MIDL2095</strong></dt> </dl></td>
<td><dl> <dt><span id="interface_name_specified_in_the_ACF_does_not_match_that_specified_in_the_IDL_file"></span><span id="interface_name_specified_in_the_acf_does_not_match_that_specified_in_the_idl_file"></span><span id="INTERFACE_NAME_SPECIFIED_IN_THE_ACF_DOES_NOT_MATCH_THAT_SPECIFIED_IN_THE_IDL_FILE"></span>Il nome dell'interfaccia specificato in ACF non corrisponde a quello specificato nel file IDL</dt> <dd> Nella modalità del compilatore corrente, il nome che segue la parola chiave interface in ACF deve corrispondere al nome che segue la parola chiave interface nel file IDL. I nomi delle interfacce nei file IDL e ACF possono essere diversi quando si esegue la compilazione con l'opzione del compilatore MIDL <a href="-acf.md"><strong>/acf</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2096"></span><span id="midl2096"></span><dl> <dt><strong>MIDL2096</strong></dt> </dl></td>
<td><dl> <dt><span id="duplicated_attribute"></span><span id="DUPLICATED_ATTRIBUTE"></span>attributo duplicato</dt> <dd> Sono stati specificati attributi duplicati o in conflitto. Questo errore si verifica spesso quando due attributi si escludono a vicenda. Ad esempio, gli attributi [<a href="code.md"><strong>code</strong></a>] e [<a href="nocode.md"><strong>nocode</strong></a>] non possono essere usati contemporaneamente.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2097"></span><span id="midl2097"></span><dl> <dt><strong>MIDL2097</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_with__comm_status__or__fault_status__attribute_must_be_a_pointer_to_type_error_status_t"></span><span id="PARAMETER_WITH__COMM_STATUS__OR__FAULT_STATUS__ATTRIBUTE_MUST_BE_A_POINTER_TO_TYPE_ERROR_STATUS_T"></span>il parametro con l'attributo [comm_status] o [fault_status] deve essere un puntatore al tipo error_status_t</dt> <dd> Quando [<a href="fault-status.md"><strong>fault_status</strong></a>] o [<a href="comm-status.md"><strong>comm_status</strong></a>] viene usato come attributo di parametro, il parametro deve essere un parametro [<a href="out-idl.md"><strong>out</strong></a>] di <a href="error-status-t.md"><strong>tipo error_status_t</strong></a>. Se si verifica un errore del server, il parametro viene impostato sul codice di errore. Quando la chiamata remota viene completata correttamente, la procedura imposta il valore .<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2098"></span><span id="midl2098"></span><dl> <dt><strong>MIDL2098</strong></dt> </dl></td>
<td><dl> <dt><span id="a__local__procedure_cannot_be_specified_in_ACF_file"></span><span id="a__local__procedure_cannot_be_specified_in_acf_file"></span><span id="A__LOCAL__PROCEDURE_CANNOT_BE_SPECIFIED_IN_ACF_FILE"></span>Impossibile specificare una routine [local] nel file ACF</dt> <dd> Nel file ACF è stata specificata una procedura locale. La procedura locale può essere specificata solo nel file IDL.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2099"></span><span id="midl2099"></span><dl> <dt><strong>MIDL2099</strong></dt> </dl></td>
<td><dl> <dt><span id="specified_type_is_not_defined_as_a_handle"></span><span id="SPECIFIED_TYPE_IS_NOT_DEFINED_AS_A_HANDLE"></span>il tipo specificato non è definito come handle</dt> <dd> Il tipo specificato<a href="implicit-handle.md"><strong>nell'attributo</strong></a>[ implicit_handle ] non è definito come tipo di handle. Modificare la definizione del tipo o il nome del tipo specificato dall'attributo .<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2100"></span><span id="midl2100"></span><dl> <dt><strong>MIDL2100</strong></dt> </dl></td>
<td><dl> <dt><span id="procedure_undefined"></span><span id="PROCEDURE_UNDEFINED"></span>procedura non definita</dt> <dd> Un attributo è stato applicato a una routine in ACF e tale procedura non è definita nel file IDL.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2101"></span><span id="midl2101"></span><dl> <dt><strong>MIDL2101</strong></dt> </dl></td>
<td><dl> <dt><span id="this_parameter_does_not_exist_in_the_IDL_file"></span><span id="this_parameter_does_not_exist_in_the_idl_file"></span><span id="THIS_PARAMETER_DOES_NOT_EXIST_IN_THE_IDL_FILE"></span>questo parametro non esiste nel file IDL</dt> <dd> Un parametro specificato in ACF non esiste nella definizione nel file IDL. Tutti i parametri, le funzioni e le definizioni dei tipi visualizzati nel file ACF devono corrispondere a parametri, funzioni e tipi definiti in precedenza nel file IDL.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2102"></span><span id="midl2102"></span><dl> <dt><strong>MIDL2102</strong></dt> </dl></td>
<td><dl> <dt><span id="this_array-bounds_construct_is_not_supported"></span><span id="THIS_ARRAY-BOUNDS_CONSTRUCT_IS_NOT_SUPPORTED"></span>Questo costrutto di limiti di matrice non è supportato</dt> <dd> MIDL attualmente supporta l'espressione dei limiti superiore e inferiore di una matrice nel formato Array[Lower .. Upper] solo quando la costante che specifica il limite inferiore della matrice viene risolta nel valore zero.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2103"></span><span id="midl2103"></span><dl> <dt><strong>MIDL2103</strong></dt> </dl></td>
<td><dl> <dt><span id="array_bound_specification_is_illegal"></span><span id="ARRAY_BOUND_SPECIFICATION_IS_ILLEGAL"></span>La specifica del limite di matrici non è valida</dt> <dd> La specifica utente dei limiti di matrice per la matrice di dimensioni fisse non è valida. Esempio: <br/>
<pre class="syntax" data-space="preserve"><code>typedef short Array[-1]</code></pre>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2104"></span><span id="midl2104"></span><dl> <dt><strong>MIDL2104</strong></dt> </dl></td>
<td><dl> <dt><span id="pointer_to_a_conformant_array_or_an_array_that_contains_a_conformant_array_is_not_supported"></span><span id="POINTER_TO_A_CONFORMANT_ARRAY_OR_AN_ARRAY_THAT_CONTAINS_A_CONFORMANT_ARRAY_IS_NOT_SUPPORTED"></span>Il puntatore a una matrice conforme o a una matrice contenente una matrice conforme non è supportato</dt> <dd> Utilizzo della matrice conforme non valido. Per le regole che regolano le matrici conformi, vedere <a href="/windows/desktop/Rpc/arrays-and-rpc">Matrici e RPC.</a><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2105"></span><span id="midl2105"></span><dl> <dt><strong>MIDL2105</strong></dt> </dl></td>
<td><dl> <dt><span id="pointee_array_does_not_derive_any_size"></span><span id="POINTEE_ARRAY_DOES_NOT_DERIVE_ANY_SIZE"></span>pointee/array non deriva alcuna dimensione</dt> <dd> È stata specificata una matrice conforme senza alcuna specifica delle dimensioni. È possibile specificare le dimensioni con<a href="max-is.md"><strong>l'attributo</strong></a>[ max_is ] o [<a href="size-is.md"><strong>size_is</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2106"></span><span id="midl2106"></span><dl> <dt><strong>MIDL2106</strong></dt> </dl></td>
<td><dl> <dt><span id="only_fixed_arrays_and_SAFEARRAYs_are_legal_in_a_type_library"></span><span id="only_fixed_arrays_and_safearrays_are_legal_in_a_type_library"></span><span id="ONLY_FIXED_ARRAYS_AND_SAFEARRAYS_ARE_LEGAL_IN_A_TYPE_LIBRARY"></span>solo le matrici fisse e SAFEARRAY sono legali in una libreria dei tipi</dt> <dd> È stato usato un tipo matrice all'interno di un'istruzione di libreria che non può essere usata in una libreria dei tipi.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2107"></span><span id="midl2107"></span><dl> <dt><strong>MIDL2107</strong></dt> </dl></td>
<td><dl> <dt><span id="SAFEARRAYs_are_only_legal_inside_a_library_block"></span><span id="safearrays_are_only_legal_inside_a_library_block"></span><span id="SAFEARRAYS_ARE_ONLY_LEGAL_INSIDE_A_LIBRARY_BLOCK"></span>SAFEARRAYs è legale solo all'interno di un blocco di libreria</dt> <dd> Il compilatore MIDL non riconosce SAFEARRAY come tipo di dati valido, se non durante la generazione di una libreria dei tipi.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2108"></span><span id="midl2108"></span><dl> <dt><strong>MIDL2108</strong></dt> </dl></td>
<td><dl> <dt><span id="badly_formed_character_constant"></span><span id="BADLY_FORMED_CHARACTER_CONSTANT"></span>Costante di caratteri con formato non corretto</dt> <dd> Il carattere di fine riga non è consentito nelle costanti carattere.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2109"></span><span id="midl2109"></span><dl> <dt><strong>MIDL2109</strong></dt> </dl></td>
<td><dl> <dt><span id="end_of_file_found_in_comment"></span><span id="END_OF_FILE_FOUND_IN_COMMENT"></span>fine del file trovata nel commento</dt> <dd> Il carattere di fine file è stato rilevato in un commento.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2110"></span><span id="midl2110"></span><dl> <dt><strong>MIDL2110</strong></dt> </dl></td>
<td><dl> <dt><span id="end_of_file_found_in_string"></span><span id="END_OF_FILE_FOUND_IN_STRING"></span>fine del file trovata nella stringa</dt> <dd> Il carattere di fine file è stato rilevato in una stringa.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2111"></span><span id="midl2111"></span><dl> <dt><strong>MIDL2111</strong></dt> </dl></td>
<td><dl> <dt><span id="identifier_length_exceeds_31_characters"></span><span id="IDENTIFIER_LENGTH_EXCEEDS_31_CHARACTERS"></span>La lunghezza dell'identificatore supera i 31 caratteri</dt> <dd> Gli identificatori sono limitati a 31 caratteri alfanumerici. I nomi degli identificatori di lunghezza superiore a 31 caratteri vengono troncati.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2112"></span><span id="midl2112"></span><dl> <dt><strong>MIDL2112</strong></dt> </dl></td>
<td><dl> <dt><span id="end_of_line_found_in_string"></span><span id="END_OF_LINE_FOUND_IN_STRING"></span>fine della riga trovata nella stringa</dt> <dd> Il carattere di fine riga è stato rilevato nella stringa. Verificare di aver incluso il carattere virgolette doppie che termina la stringa.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2113"></span><span id="midl2113"></span><dl> <dt><strong>MIDL2113</strong></dt> </dl></td>
<td><dl> <dt><span id="string_constant_exceeds_limit_of_255_characters"></span><span id="STRING_CONSTANT_EXCEEDS_LIMIT_OF_255_CHARACTERS"></span>La costante stringa supera il limite di 255 caratteri</dt> <dd> La stringa ha superato la lunghezza massima consentita di 255 caratteri.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2114"></span><span id="midl2114"></span><dl> <dt><strong>MIDL2114</strong></dt> </dl></td>
<td><dl> <dt><span id="identifier_exceeds_limit_of_255_characters_and_has_been_truncated"></span><span id="IDENTIFIER_EXCEEDS_LIMIT_OF_255_CHARACTERS_AND_HAS_BEEN_TRUNCATED"></span>l'identificatore supera il limite di 255 caratteri ed è stato troncato</dt> <dd> L'identificatore ha superato la lunghezza massima consentita di 255 caratteri. I caratteri in eccesso nell'identificatore vengono troncati.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2115"></span><span id="midl2115"></span><dl> <dt><strong>MIDL2115</strong></dt> </dl></td>
<td><dl> <dt><span id="constant_too_big"></span><span id="CONSTANT_TOO_BIG"></span>costante troppo grande</dt> <dd> La costante è troppo grande per essere rappresentata internamente.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2116"></span><span id="midl2116"></span><dl> <dt><strong>MIDL2116</strong></dt> </dl></td>
<td><dl> <dt><span id="numerical_parsing_error"></span><span id="NUMERICAL_PARSING_ERROR"></span>Errore di analisi numerica</dt> <dd> Il compilatore non è riuscito ad analizzare l'identificatore numerico.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2117"></span><span id="midl2117"></span><dl> <dt><strong>MIDL2117</strong></dt> </dl></td>
<td><dl> <dt><span id="error_in_opening_file"></span><span id="ERROR_IN_OPENING_FILE"></span>errore durante l'apertura del file</dt> <dd> Il sistema operativo ha segnalato un errore durante il tentativo di aprire un file di output. Questo errore può essere causato da un nome troppo lungo per l'file system o da un nome file duplicato.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2118"></span><span id="midl2118"></span><dl> <dt><strong>MIDL2118</strong></dt> </dl></td>
<td>errore durante l'associazione alla funzione<br/></td>
</tr>
<tr class="even">
<td><span id="MIDL2119"></span><span id="midl2119"></span><dl> <dt><strong>MIDL2119</strong></dt> </dl></td>
<td>errore durante l'inizializzazione di OLE<br/></td>
</tr>
<tr class="odd">
<td><span id="MIDL2120"></span><span id="midl2120"></span><dl> <dt><strong>MIDL2120</strong></dt> </dl></td>
<td>errore durante il caricamento della libreria<br/></td>
</tr>
<tr class="even">
<td><span id="MIDL2121"></span><span id="midl2121"></span><dl> <dt><strong>MIDL2121</strong></dt> </dl></td>
<td><dl> <dt><span id="_out__only_parameter_must_not_derive_from_a_top-level__unique__or__ptr__pointer_array"></span><span id="_OUT__ONLY_PARAMETER_MUST_NOT_DERIVE_FROM_A_TOP-LEVEL__UNIQUE__OR__PTR__POINTER_ARRAY"></span>[out] solo il parametro non deve derivare da un puntatore/matrice [unique] o [ptr] di primo livello</dt> <dd> Un puntatore univoco non può essere un parametro [<a href="out-idl.md"><strong>out</strong></a>]-only. Per definizione, un puntatore univoco può passare da <strong>NULL</strong> a non<strong>NULL.</strong> Nessuna informazione sul parametro [<strong>out</strong>]-only viene passata dal client al server.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2122"></span><span id="midl2122"></span><dl> <dt><strong>MIDL2122</strong></dt> </dl></td>
<td><dl> <dt><span id="attribute_is_not_applicable_to_this_non-rpcable_union"></span><span id="ATTRIBUTE_IS_NOT_APPLICABLE_TO_THIS_NON-RPCABLE_UNION"></span>l'attributo non è applicabile a questa unione non rpcable</dt> <dd> Solo gli attributi [<a href="switch-is.md"><strong>switch_is</strong></a>] e [<a href="switch-type.md"><strong>switch_type</strong></a>] si applicano a un'unione trasmessa come parte di una chiamata di procedura remota.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2123"></span><span id="midl2123"></span><dl> <dt><strong>MIDL2123</strong></dt> </dl></td>
<td><dl> <dt><span id="expression_used_for_a_size_attribute_must_not_derive_from_an__out_-only_parameter"></span><span id="EXPRESSION_USED_FOR_A_SIZE_ATTRIBUTE_MUST_NOT_DERIVE_FROM_AN__OUT_-ONLY_PARAMETER"></span>L'espressione usata per un attributo size non deve derivare da un parametro [out]-only</dt> <dd> Il valore di un parametro [<a href="out-idl.md"><strong>out</strong></a>]-only non viene trasmesso al server e non può essere usato per determinare la lunghezza o le dimensioni del parametro [<a href="in.md"><strong>in</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2124"></span><span id="midl2124"></span><dl> <dt><strong>MIDL2124</strong></dt> </dl></td>
<td><dl> <dt><span id="expression_used_for_a_length_attribute_for_an__in__parameter_cannot_derive_from_an__out_-only_parameter"></span><span id="EXPRESSION_USED_FOR_A_LENGTH_ATTRIBUTE_FOR_AN__IN__PARAMETER_CANNOT_DERIVE_FROM_AN__OUT_-ONLY_PARAMETER"></span>L'espressione usata per un attributo length per un parametro [in] non può derivare da un parametro [out]-only</dt> <dd> Il valore di un parametro [<a href="out-idl.md"><strong>out</strong></a>]-only non viene trasmesso al server e non può essere usato per determinare la lunghezza o le dimensioni del parametro [<a href="in.md"><strong>in</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2125"></span><span id="midl2125"></span><dl> <dt><strong>MIDL2125</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of__int__needs__c_ext"></span><span id="USE_OF__INT__NEEDS__C_EXT"></span>l'uso &quot; di int &quot; needs /c_ext</dt> <dd> MIDL è un linguaggio fortemente tipizzato. Tutti i parametri trasmessi in rete devono essere derivati da uno dei tipi di base MIDL. Il tipo <a href="int.md"><strong>int</strong></a> non è definito come parte di MIDL. I dati trasmessi devono includere un identificatore di dimensioni: <a href="small.md"><strong>small</strong></a>, <strong>short</strong>o <strong>long</strong>. I dati non trasmessi in rete possono essere inclusi in un'interfaccia. usare <a href="-c-ext.md"><strong>l'opzione /c_ext.</strong></a><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2126"></span><span id="midl2126"></span><dl> <dt><strong>MIDL2126</strong></dt> </dl></td>
<td><dl> <dt><span id="struct_union_field_must_not_be__void_"></span><span id="STRUCT_UNION_FIELD_MUST_NOT_BE__VOID_"></span>Il campo struct/union non deve essere &quot; void&quot;</dt> <dd> I campi di una struttura o di un'unione devono essere dichiarati come di un tipo di base specifico supportato da MIDL o da un tipo derivato dai tipi di base. I tipi Void non sono consentiti nelle operazioni remote.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2127"></span><span id="midl2127"></span><dl> <dt><strong>MIDL2127</strong></dt> </dl></td>
<td><dl> <dt><span id="array_element_must_not_be_void"></span><span id="ARRAY_ELEMENT_MUST_NOT_BE_VOID"></span>L'elemento array non deve essere void</dt> <dd> Un elemento della matrice non può essere void.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2128"></span><span id="midl2128"></span><dl> <dt><strong>MIDL2128</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of_type_qualifiers_and_or_modifiers_needs__c_ext"></span><span id="USE_OF_TYPE_QUALIFIERS_AND_OR_MODIFIERS_NEEDS__C_EXT"></span>L'uso di qualificatori di tipo e/o modificatori richiede /c_ext</dt> <dd> I modificatori di tipo <strong>_cdecl</strong> <strong>e _far</strong> possono essere compilati solo se si specifica l'opzione <a href="-c-ext.md"><strong>/c_ext.</strong></a><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2129"></span><span id="midl2129"></span><dl> <dt><strong>MIDL2129</strong></dt> </dl></td>
<td><dl> <dt><span id="struct_union_field_must_not_derive_from_a_function"></span><span id="STRUCT_UNION_FIELD_MUST_NOT_DERIVE_FROM_A_FUNCTION"></span>Il campo struct/union non deve derivare da una funzione</dt> <dd> I campi di una struttura o di un'unione devono essere tipi di base MIDL o tipi derivati da questi tipi di base. Le funzioni non sono legali nei campi di struttura o unione.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2130"></span><span id="midl2130"></span><dl> <dt><strong>MIDL2130</strong></dt> </dl></td>
<td><dl> <dt><span id="array_element_must_not_be_a_function"></span><span id="ARRAY_ELEMENT_MUST_NOT_BE_A_FUNCTION"></span>L'elemento array non deve essere una funzione</dt> <dd> Un elemento della matrice non può essere una funzione.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2131"></span><span id="midl2131"></span><dl> <dt><strong>MIDL2131</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_must_not_be_a_function"></span><span id="PARAMETER_MUST_NOT_BE_A_FUNCTION"></span>il parametro non deve essere una funzione</dt> <dd> Il parametro di una procedura remota deve essere una variabile di un tipo specificato. Una funzione non può essere un parametro della procedura remota.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2132"></span><span id="midl2132"></span><dl> <dt><strong>MIDL2132</strong></dt> </dl></td>
<td><dl> <dt><span id="struct_union_with_bit_fields_needs__c_ext"></span><span id="STRUCT_UNION_WITH_BIT_FIELDS_NEEDS__C_EXT"></span>struct/union con campi di bit richiede /c_ext</dt> <dd> È necessario specificare l'opzione <a href="-c-ext.md"><strong>/c_ext</strong></a> del compilatore MIDL per consentire i campi di bit nelle strutture che non vengono trasmessi in una chiamata di procedura remota.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2133"></span><span id="midl2133"></span><dl> <dt><strong>MIDL2133</strong></dt> </dl></td>
<td><dl> <dt><span id="bit_field_specification_on_a_type_other_that__int__is_a_non-ANSI-compatible_extension"></span><span id="bit_field_specification_on_a_type_other_that__int__is_a_non-ansi-compatible_extension"></span><span id="BIT_FIELD_SPECIFICATION_ON_A_TYPE_OTHER_THAT__INT__IS_A_NON-ANSI-COMPATIBLE_EXTENSION"></span>specifica del campo di bit in un tipo diverso da &quot; int &quot; è un'estensione non compatibile con ANSI</dt> <dd> La specifica del linguaggio di programmazione ANSI C non consente l'applicazione di campi di bit a tipi non integer.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2134"></span><span id="midl2134"></span><dl> <dt><strong>MIDL2134</strong></dt> </dl></td>
<td><dl> <dt><span id="bit_field_specification_can_be_applied_only_to_simple__integral_types"></span><span id="BIT_FIELD_SPECIFICATION_CAN_BE_APPLIED_ONLY_TO_SIMPLE__INTEGRAL_TYPES"></span>La specifica del campo di bit può essere applicata solo a tipi semplici e integrali</dt> <dd> La specifica del linguaggio di programmazione ANSI C non consente l'applicazione di campi di bit a tipi non integer.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2135"></span><span id="midl2135"></span><dl> <dt><strong>MIDL2135</strong></dt> </dl></td>
<td><dl> <dt><span id="struct_union_field_must_not_derive_from_handle_t_or_a_context-handle"></span><span id="STRUCT_UNION_FIELD_MUST_NOT_DERIVE_FROM_HANDLE_T_OR_A_CONTEXT-HANDLE"></span>Il campo struct/union non deve derivare da handle_t o da un handle di contesto</dt> <dd> Gli handle di contesto non possono essere trasmessi come parte di un'altra struttura. Devono essere trasmessi come handle di contesto.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2136"></span><span id="midl2136"></span><dl> <dt><strong>MIDL2136</strong></dt> </dl></td>
<td><dl> <dt><span id="array_element_must_not_derive_from_handle_t_or_a_context_handle"></span><span id="ARRAY_ELEMENT_MUST_NOT_DERIVE_FROM_HANDLE_T_OR_A_CONTEXT_HANDLE"></span>L'elemento array non deve derivare da handle_t o da un handle di contesto</dt> <dd> Gli handle di contesto non possono essere trasmessi come parte di una matrice.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2137"></span><span id="midl2137"></span><dl> <dt><strong>MIDL2137</strong></dt> </dl></td>
<td><dl> <dt><span id="this_specification_of_union_needs__c_ext"></span><span id="THIS_SPECIFICATION_OF_UNION_NEEDS__C_EXT"></span>questa specifica dell'unione richiede /c_ext</dt> <dd> Un'unione visualizzata nella definizione dell'interfaccia deve essere associata al discriminante o dichiarata come locale. I dati non trasmessi in rete possono essere dichiarati in modo implicito come locali quando si usa l'opzione <a href="-c-ext.md"><strong>/c_ext,</strong></a> che è l'impostazione predefinita MIDL. Non è possibile compilare questo file IDL con <a href="-osf.md"><strong>l'opzione /osf.</strong></a><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2138"></span><span id="midl2138"></span><dl> <dt><strong>MIDL2138</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_deriving_from_an__int__must_have_size_specifier__small____short___or__long__with_the__int_"></span><span id="PARAMETER_DERIVING_FROM_AN__INT__MUST_HAVE_SIZE_SPECIFIER__SMALL____SHORT___OR__LONG__WITH_THE__INT_"></span>il parametro derivante da un int deve avere l'identificatore di dimensione &quot; &quot; &quot; &quot; &quot; small, short &quot; o long con &quot; &quot; &quot; int&quot;</dt> <dd> Il tipo <a href="int.md"><strong>int</strong></a> è solo un tipo MIDL valido nelle piattaforme a 32 bit. Nei sistemi a 16 bit <strong>int</strong> deve essere accompagnato da una specifica delle dimensioni. Usare uno degli identificatori di dimensione <a href="small.md"><strong>small</strong></a>, <a href="short.md"><strong>short</strong></a>o <a href="long.md"><strong>long</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2139"></span><span id="midl2139"></span><dl> <dt><strong>MIDL2139</strong></dt> </dl></td>
<td><dl> <dt><span id="type_of_the_parameter_cannot_derive_from_void_or_void_"></span><span id="TYPE_OF_THE_PARAMETER_CANNOT_DERIVE_FROM_VOID_OR_VOID_"></span>Il tipo del parametro non può derivare da void o void*</dt> <dd> MIDL è un linguaggio fortemente tipizzato. Tutti i parametri trasmessi in rete devono essere derivati da uno dei tipi di base MIDL. MIDL non supporta <a href="void.md"><strong>void</strong></a> come tipo di base. È necessario modificare la dichiarazione in un tipo MIDL valido.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2140"></span><span id="midl2140"></span><dl> <dt><strong>MIDL2140</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_deriving_from_a_struct_union_containing_bit_fields_is_not_supported"></span><span id="PARAMETER_DERIVING_FROM_A_STRUCT_UNION_CONTAINING_BIT_FIELDS_IS_NOT_SUPPORTED"></span>Il parametro derivante da uno struct/unione contenente campi di bit non è supportato</dt> <dd> I campi di bit non sono definiti come tipo di dati valido da RPC DCE.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2141"></span><span id="midl2141"></span><dl> <dt><strong>MIDL2141</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of_a_parameter_deriving_from_a_type_containing_type-modifiers_type-qualifiers_needs__c_ext"></span><span id="USE_OF_A_PARAMETER_DERIVING_FROM_A_TYPE_CONTAINING_TYPE-MODIFIERS_TYPE-QUALIFIERS_NEEDS__C_EXT"></span>L'uso di un parametro derivante da un tipo contenente modificatori di tipo/qualificatori di tipo richiede /c_ext</dt> <dd> L'uso di parole chiave come <strong>far</strong>, <strong>near</strong>, <a href="const.md"><strong>const</strong></a>e <strong>volatile</strong> nel file IDL è un'estensione Microsoft per DCE RPC. Queste parole chiave non sono disponibili quando si esegue la compilazione con l'opzione <a href="-osf.md"><strong>/osf,</strong></a> che disattiva l'opzione <a href="-c-ext.md"><strong>di estensione /c_ext</strong></a> predefinita.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2142"></span><span id="midl2142"></span><dl> <dt><strong>MIDL2142</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_must_not_derive_from_a_pointer_to_a_function"></span><span id="PARAMETER_MUST_NOT_DERIVE_FROM_A_POINTER_TO_A_FUNCTION"></span>il parametro non deve derivare da un puntatore a una funzione</dt> <dd> Le librerie di runtime RPC trasmettono un puntatore e i dati associati tra client e server. I puntatori alle funzioni non possono essere trasmessi come parametri perché la funzione non può essere trasmessa in rete.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2143"></span><span id="midl2143"></span><dl> <dt><strong>MIDL2143</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_must_not_derive_from_a_nonrpccapable_union"></span><span id="PARAMETER_MUST_NOT_DERIVE_FROM_A_NONRPCCAPABLE_UNION"></span>il parametro non deve derivare da un'unione che supporta nonrpc</dt> <dd> L'unione deve essere associata a un oggetto discriminante. Usare gli attributi [<a href="switch-is.md"><strong>switch_is</strong></a>] e [<a href="switch-type.md"><strong>switch_type</strong></a>] .<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2144"></span><span id="midl2144"></span><dl> <dt><strong>MIDL2144</strong></dt> </dl></td>
<td><dl> <dt><span id="return_type_derives_from_an__int.__You_must_use_size_specifiers_with_the__int_"></span><span id="return_type_derives_from_an__int.__you_must_use_size_specifiers_with_the__int_"></span><span id="RETURN_TYPE_DERIVES_FROM_AN__INT.__YOU_MUST_USE_SIZE_SPECIFIERS_WITH_THE__INT_"></span>il tipo restituito deriva da un &quot; int. &quot; È necessario usare gli identificatori di dimensione con &quot; int&quot;</dt> <dd> Nei sistemi a 16 bit il tipo <a href="int.md"><strong>int</strong></a> non è un tipo MIDL valido a meno che non sia accompagnato da una specifica delle dimensioni. Usare uno degli identificatori di dimensione <a href="small.md"><strong>small</strong></a>, <a href="short.md"><strong>short</strong></a>o <a href="long.md"><strong>long</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2145"></span><span id="midl2145"></span><dl> <dt><strong>MIDL2145</strong></dt> </dl></td>
<td><dl> <dt><span id="return_type_must_not_derive_from_a_void_pointer"></span><span id="RETURN_TYPE_MUST_NOT_DERIVE_FROM_A_VOID_POINTER"></span>Il tipo restituito non deve derivare da un puntatore void</dt> <dd> MIDL è un linguaggio fortemente tipizzato. Tutti i parametri trasmessi in rete devono essere derivati da uno dei tipi di base MIDL. I tipi Void non sono definiti come parte di MIDL. È necessario modificare la dichiarazione in un tipo MIDL valido.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2146"></span><span id="midl2146"></span><dl> <dt><strong>MIDL2146</strong></dt> </dl></td>
<td><dl> <dt><span id="return_type_must_not_derive_from_a_structure_union_containing_bit-fields"></span><span id="RETURN_TYPE_MUST_NOT_DERIVE_FROM_A_STRUCTURE_UNION_CONTAINING_BIT-FIELDS"></span>Il tipo restituito non deve derivare da una struttura/unione contenente campi di bit</dt> <dd> I campi di bit non sono definiti come tipo di dati valido da RPC DCE.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2147"></span><span id="midl2147"></span><dl> <dt><strong>MIDL2147</strong></dt> </dl></td>
<td><dl> <dt><span id="return_type_must_not_derive_from_a_nonrpccapable_union"></span><span id="RETURN_TYPE_MUST_NOT_DERIVE_FROM_A_NONRPCCAPABLE_UNION"></span>Il tipo restituito non deve derivare da un'unione che supporta nonrpc</dt> <dd> L'unione deve essere associata a un oggetto discriminante. Usare gli attributi [<a href="switch-is.md"><strong>switch_is</strong></a>] e [<a href="switch-type.md"><strong>switch_type</strong></a>] .<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2148"></span><span id="midl2148"></span><dl> <dt><strong>MIDL2148</strong></dt> </dl></td>
<td><dl> <dt><span id="return_type_must_not_derive_from_a_pointer_to_a_function"></span><span id="RETURN_TYPE_MUST_NOT_DERIVE_FROM_A_POINTER_TO_A_FUNCTION"></span>Il tipo restituito non deve derivare da un puntatore a una funzione</dt> <dd> Le librerie di runtime RPC trasmettono un puntatore e i dati associati tra client e server. I puntatori alle funzioni non possono essere trasmessi come parametri perché RPC non definisce un metodo per trasmettere la funzione associata in rete.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2149"></span><span id="midl2149"></span><dl> <dt><strong>MIDL2149</strong></dt> </dl></td>
<td><dl> <dt><span id="compound_initializers_are_not_supported"></span><span id="COMPOUND_INITIALIZERS_ARE_NOT_SUPPORTED"></span>Gli inizializzatori composti non sono supportati</dt> <dd> DCE RPC supporta solo l'inizializzazione semplice. Impossibile inizializzare la struttura o la matrice nel file IDL.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2150"></span><span id="midl2150"></span><dl> <dt><strong>MIDL2150</strong></dt> </dl></td>
<td><dl> <dt><span id="ACF_attributes_in_the_IDL_file_need_the__app_config_switch"></span><span id="acf_attributes_in_the_idl_file_need_the__app_config_switch"></span><span id="ACF_ATTRIBUTES_IN_THE_IDL_FILE_NEED_THE__APP_CONFIG_SWITCH"></span>Gli attributi ACF nel file IDL necessitano dell'opzione /app_config</dt> <dd> Un'estensione Microsoft consente di specificare gli attributi ACF nel file IDL. Usare <a href="-app-config.md"><strong>l'opzione /app_config</strong></a> per attivare questa estensione.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2151"></span><span id="midl2151"></span><dl> <dt><strong>MIDL2151</strong></dt> </dl></td>
<td><dl> <dt><span id="single-line_comment_needs__ms_ext_or__c_ext"></span><span id="SINGLE-LINE_COMMENT_NEEDS__MS_EXT_OR__C_EXT"></span>il commento a riga singola richiede /ms_ext o /c_ext</dt> <dd> I commenti a riga singola che usano due caratteri barra (//) rappresentano un'estensione Microsoft per DCE RPC. Non è possibile usare commenti a riga singola se si esegue la compilazione con <a href="-osf.md"><strong>l'opzione /osf.</strong></a><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2152"></span><span id="midl2152"></span><dl> <dt><strong>MIDL2152</strong></dt> </dl></td>
<td><dl> <dt><span id="_version__format_is_incorrect"></span><span id="_VERSION__FORMAT_IS_INCORRECT"></span>Il formato [versione] non è corretto</dt> <dd> Il numero di versione dell'interfaccia nell'intestazione dell'interfaccia deve essere specificato nel formato <em>principale</em>. <em>minor</em>, in cui ogni numero può essere compreso tra 0 e 65535.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2153"></span><span id="midl2153"></span><dl> <dt><strong>MIDL2153</strong></dt> </dl></td>
<td><dl> <dt><span id="_signed__needs__ms_ext_or__c_ext"></span><span id="_SIGNED__NEEDS__MS_EXT_OR__C_EXT"></span>&quot;signed &quot; richiede /ms_ext o /c_ext</dt> <dd> L'uso della parola <a href="signed.md"><strong>chiave signed</strong></a> è un'estensione Microsoft per DCE RPC. Non è possibile usare <a href="-osf.md"><strong>l'opzione /osf</strong></a> se si vuole usare questa funzionalità.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2154"></span><span id="midl2154"></span><dl> <dt><strong>MIDL2154</strong></dt> </dl></td>
<td><dl> <dt><span id="mismatch_in_assignment_type"></span><span id="MISMATCH_IN_ASSIGNMENT_TYPE"></span>mancata corrispondenza nel tipo di assegnazione</dt> <dd> Il tipo della variabile non corrisponde al tipo del valore assegnato alla variabile.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2155"></span><span id="midl2155"></span><dl> <dt><strong>MIDL2155</strong></dt> </dl></td>
<td><dl> <dt><span id="declaration_must_be_of_the_form__const__type__declarator_____initializing_expression_"></span><span id="DECLARATION_MUST_BE_OF_THE_FORM__CONST__TYPE__DECLARATOR_____INITIALIZING_EXPRESSION_"></span>la dichiarazione deve avere il formato: const <type><declarator> = <initializing expression></dt> <dd> La dichiarazione non è compatibile con la sintassi RPC DCE. Usare <a href="-ms-ext.md"><strong>l'opzione /ms_ext</strong></a> <a href="-c-ext.md"><strong>o /c_ext</strong></a> modalità del compilatore MIDL.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2156"></span><span id="midl2156"></span><dl> <dt><strong>MIDL2156</strong></dt> </dl></td>
<td><dl> <dt><span id="declaration_must_have__const_"></span><span id="DECLARATION_MUST_HAVE__CONST_"></span>la dichiarazione deve avere &quot; const&quot;</dt> <dd> Le dichiarazioni nel file IDL devono essere espressioni costanti che usano la parola chiave <a href="const.md"><strong>const</strong></a>, ad esempio:<br/>
<pre class="syntax" data-space="preserve"><code>const short x = 2;</code></pre>
</dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2157"></span><span id="midl2157"></span><dl> <dt><strong>MIDL2157</strong></dt> </dl></td>
<td><dl> <dt><span id="struct_union_enum_must_not_be_defined_in_a_parameter-type_specification"></span><span id="STRUCT_UNION_ENUM_MUST_NOT_BE_DEFINED_IN_A_PARAMETER-TYPE_SPECIFICATION"></span>struct/union/enum non deve essere definito in una specifica del tipo di parametro</dt> <dd> La struttura, l'unione o il tipo enumerato devono essere dichiarati in modo esplicito all'esterno del prototipo di funzione.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2158"></span><span id="midl2158"></span><dl> <dt><strong>MIDL2158</strong></dt> </dl></td>
<td><dl> <dt><span id="_allocate__attribute_must_be_applied_only_on_non-void_pointer_types"></span><span id="_ALLOCATE__ATTRIBUTE_MUST_BE_APPLIED_ONLY_ON_NON-VOID_POINTER_TYPES"></span>L'attributo [allocate] deve essere applicato solo a tipi puntatore non void</dt> <dd> <a href="allocate.md"><strong>L'attributo</strong></a>[ allocate ] è progettato per strutture di dati complesse basate su puntatore. Quando viene specificato l'attributo [allocate], il file stub attraversa la struttura dei dati per calcolare le dimensioni totali di tutti gli oggetti accessibili dal puntatore e da tutti gli altri puntatori nella struttura dei dati. Modificare il tipo in un tipo di puntatore nonvoid o rimuovere l'attributo [<strong>allocate</strong>] e usare un altro metodo per determinarne le dimensioni di allocazione, ad esempio <strong>l'operatore sizeof.</strong><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2159"></span><span id="midl2159"></span><dl> <dt><strong>MIDL2159</strong></dt> </dl></td>
<td><dl> <dt><span id="array_or_equivalent_pointer_construct_cannot_derive_from_a_nonencapsulated_union"></span><span id="ARRAY_OR_EQUIVALENT_POINTER_CONSTRUCT_CANNOT_DERIVE_FROM_A_NONENCAPSULATED_UNION"></span>Il costrutto di matrice o di puntatore equivalente non può derivare da un'unione non incapsulata</dt> <dd> Ogni unione deve essere associata a un oggetto discriminante. Le matrici di unioni non sono consentite perché non forniscono la discriminante associata. Le matrici di strutture in cui la struttura contiene l'unione e la relativa discriminante sono consentite perché gli stub possono usare il discriminante per determinare le dimensioni di ogni unione.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2160"></span><span id="midl2160"></span><dl> <dt><strong>MIDL2160</strong></dt> </dl></td>
<td><dl> <dt><span id="field_must_not_derive_from_an_error_status_t_type"></span><span id="FIELD_MUST_NOT_DERIVE_FROM_AN_ERROR_STATUS_T_TYPE"></span>il campo non deve derivare da un tipo error_status_t</dt> <dd> Il <a href="error-status-t.md"><strong>error_status_t</strong></a> può essere usato solo come parametro o come tipo restituito. Non può essere incorporato nel campo di una struttura o di un'unione.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2161"></span><span id="midl2161"></span><dl> <dt><strong>MIDL2161</strong></dt> </dl></td>
<td><dl> <dt><span id="union_has_at_least_one_arm_without_a_case_label"></span><span id="UNION_HAS_AT_LEAST_ONE_ARM_WITHOUT_A_CASE_LABEL"></span>union ha almeno un arm senza un'etichetta case</dt> <dd> La dichiarazione di unione non corrisponde alla sintassi MIDL richiesta per l'unione. Ogni arm di unione richiede un'etichetta case o un'etichetta predefinita che seleziona tale arm union.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2162"></span><span id="midl2162"></span><dl> <dt><strong>MIDL2162</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_or_return_value_must_not_derive_from_a_type_that_has__ignore__applied_to_it"></span><span id="PARAMETER_OR_RETURN_VALUE_MUST_NOT_DERIVE_FROM_A_TYPE_THAT_HAS__IGNORE__APPLIED_TO_IT"></span>il parametro o il valore restituito non deve derivare da un tipo a cui è applicato [ignore]</dt> <dd> <a href="ignore.md"><strong>L'attributo</strong></a>[ ignore ] è un attributo di campo che può essere applicato solo ai campi, ad esempio campi di strutture e matrici. L'attributo [<strong>ignore</strong>] indica che lo stub non deve dereferenziare il puntatore durante la trasmissione e non è consentito quando è in conflitto con altri attributi che devono essere dereferenziati, ad esempio i parametri [<a href="out-idl.md"><strong>out</strong></a>] e i valori restituiti della funzione.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2163"></span><span id="midl2163"></span><dl> <dt><strong>MIDL2163</strong></dt> </dl></td>
<td><dl> <dt><span id="pointer_already_has_a_pointer_attribute_applied_to_it"></span><span id="POINTER_ALREADY_HAS_A_POINTER_ATTRIBUTE_APPLIED_TO_IT"></span>Puntatore a cui è già stato applicato un attributo puntatore</dt> <dd> Solo uno degli attributi del puntatore, [<a href="ref.md"><strong>ref</strong></a>], [<a href="unique.md"><strong>unique</strong></a>], o [<a href="ptr.md"><strong>ptr</strong></a>], può essere applicato a un singolo puntatore.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2164"></span><span id="midl2164"></span><dl> <dt><strong>MIDL2164</strong></dt> </dl></td>
<td><dl> <dt><span id="field_parameter_must_not_derive_from_a_structure_that_is_recursive_through_a_ref_pointer"></span><span id="FIELD_PARAMETER_MUST_NOT_DERIVE_FROM_A_STRUCTURE_THAT_IS_RECURSIVE_THROUGH_A_REF_POINTER"></span>field/parameter non deve derivare da una struttura ricorsiva tramite un puntatore di riferimento</dt> <dd> Per definizione, un puntatore di riferimento non può essere impostato su <strong>NULL.</strong> Una struttura di dati ricorsiva definita con un puntatore di riferimento non ha elementi <strong>NULL</strong> e, per convenzione, non è in funzione. Usare un attributo<a href="unique.md"><strong>puntatore</strong></a>[ unique ] per consentire alla struttura di dati di specificare un <strong>elemento NULL</strong> o ridefinire la struttura dei dati come struttura di dati non ricorsiva.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2165"></span><span id="midl2165"></span><dl> <dt><strong>MIDL2165</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of_field_deriving_from_a_void_pointer_needs__c_ext"></span><span id="USE_OF_FIELD_DERIVING_FROM_A_VOID_POINTER_NEEDS__C_EXT"></span>L'uso del campo derivante da un puntatore void richiede /c_ext</dt> <dd> Il tipo <strong>void *</strong> e altri tipi e qualificatori di tipo non supportati da DCE IDL sono consentiti nel file IDL solo quando si usano le impostazioni predefinite del compilatore MIDL. <a href="-osf.md"><strong>L'uso dell'opzione /osf</strong></a> esegue l'override di questa impostazione predefinita. Se è necessario eseguire la compilazione in modalità osf-compatibility, è necessario ridefinire il tipo di puntatore.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2166"></span><span id="midl2166"></span><dl> <dt><strong>MIDL2166</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of_this_attribute_needs__ms_ext"></span><span id="USE_OF_THIS_ATTRIBUTE_NEEDS__MS_EXT"></span>L'uso di questo attributo richiede /ms_ext</dt> <dd> Questa funzionalità del linguaggio è un'estensione Microsoft per DCE IDL. Non è possibile usare questa funzionalità se si esegue la compilazione in modalità di compatibilità osf ( <a href="-osf.md"><strong>/osf</strong></a> ).<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2167"></span><span id="midl2167"></span><dl> <dt><strong>MIDL2167</strong></dt> </dl></td>
<td><dl> <dt><span id="this_attribute_only_allowed_with_new_format_type_libraries"></span><span id="THIS_ATTRIBUTE_ONLY_ALLOWED_WITH_NEW_FORMAT_TYPE_LIBRARIES"></span>questo attributo è consentito solo con nuove librerie dei tipi di formato</dt> <dd> Per usare questo attributo, è necessaria la versione di Oleaut32.dll fornita con Windows 2000 o versione successiva.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2168"></span><span id="midl2168"></span><dl> <dt><strong>MIDL2168</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of_wchar_t_needs__ms_ext_or__c_ext"></span><span id="USE_OF_WCHAR_T_NEEDS__MS_EXT_OR__C_EXT"></span>l'wchar_t richiede /ms_ext o /c_ext</dt> <dd> Il tipo di caratteri wide rappresenta un'estensione di DCE IDL. Il compilatore MIDL non accetta il tipo di caratteri wide quando si specifica <a href="-osf.md"><strong>l'opzione /osf.</strong></a><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2169"></span><span id="midl2169"></span><dl> <dt><strong>MIDL2169</strong></dt> </dl></td>
<td><dl> <dt><span id="unnamed_fields_need__ms_ext_or__c_ext"></span><span id="UNNAMED_FIELDS_NEED__MS_EXT_OR__C_EXT"></span>I campi senza nome devono essere /ms_ext o /c_ext</dt> <dd> DCE IDL non supporta l'uso di unioni o strutture senza nome incorporate in altre strutture o unioni. In DCE IDL tutti questi campi incorporati devono essere denominati. Il compilatore MIDL non ne consente l'uso quando si specifica <a href="-osf.md"><strong>l'opzione /osf.</strong></a><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2170"></span><span id="midl2170"></span><dl> <dt><strong>MIDL2170</strong></dt> </dl></td>
<td><dl> <dt><span id="unnamed_fields_can_derive_only_from_struct_union_types"></span><span id="UNNAMED_FIELDS_CAN_DERIVE_ONLY_FROM_STRUCT_UNION_TYPES"></span>I campi senza nome possono derivare solo da tipi struct/union</dt> <dd> L'estensione Microsoft al linguaggio IDL DCE che supporta i campi senza nome si applica solo alle strutture e alle unioni. È necessario assegnare un nome al campo o ridefinire il campo in modo che sia conforme a questa restrizione.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2171"></span><span id="midl2171"></span><dl> <dt><strong>MIDL2171</strong></dt> </dl></td>
<td><dl> <dt><span id="field_of_a_union_cannot_derive_from_a_conformant_varying_array_or_its_pointer_equivalent"></span><span id="FIELD_OF_A_UNION_CANNOT_DERIVE_FROM_A_CONFORMANT_VARYING_ARRAY_OR_ITS_POINTER_EQUIVALENT"></span>Il campo di un'unione non può derivare da una matrice conforme/variabile o dal relativo puntatore equivalente</dt> <dd> La matrice conforme non può essere visualizzata da sola nell'unione, ma deve essere accompagnata dal valore che specifica le dimensioni della matrice. Anziché usare la matrice come arm di unione, usare una struttura costituita dalla matrice conforme e dall'identificatore che ne specifica le dimensioni.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2172"></span><span id="midl2172"></span><dl> <dt><strong>MIDL2172</strong></dt> </dl></td>
<td><dl> <dt><span id="no__pointer_default__attribute_specified__assuming__ptr__for_all_unattributed_pointers_in_interface"></span><span id="NO__POINTER_DEFAULT__ATTRIBUTE_SPECIFIED__ASSUMING__PTR__FOR_ALL_UNATTRIBUTED_POINTERS_IN_INTERFACE"></span>nessun attributo [pointer_default] specificato, presupponendo [ptr] per tutti i puntatori senza attributi nell'interfaccia</dt> <dd> L'implementazione IDL DCE specifica che tutti i puntatori in ogni file IDL devono essere associati agli attributi del puntatore. Quando un attributo puntatore esplicito non viene assegnato al parametro o al tipo di puntatore e non viene specificato alcun attributo [<a href="pointer-default.md"><strong>pointer_default</strong></a>] nel file IDL, il <a href="ptr.md"><strong>ptr</strong></a> dell'attributo del puntatore completo viene associato al puntatore. È possibile modificare gli attributi del puntatore usando attributi puntatore espliciti, specificando un attributo [<strong>pointer_default</strong>] o specificando l'opzione <a href="-ms-ext.md"><strong>/ms_ext</strong></a> per modificare l'impostazione predefinita per i puntatori senza attributi in [<a href="unique.md"><strong>unique</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2173"></span><span id="midl2173"></span><dl> <dt><strong>MIDL2173</strong></dt> </dl></td>
<td><dl> <dt><span id="initializing_expression_must_resolve_to_a_constant_expression"></span><span id="INITIALIZING_EXPRESSION_MUST_RESOLVE_TO_A_CONSTANT_EXPRESSION"></span>L'espressione di inizializzazione deve essere risolta in un'espressione costante</dt> <dd> Se un'espressione viene usata come inizializzatore, l'espressione deve essere un'espressione costante. Questo vale in tutte le modalità del compilatore MIDL. L'espressione deve essere risolvibile in fase di compilazione. Specificare una costante letterale o un'espressione che si risolve in una costante, anziché in una variabile.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2174"></span><span id="midl2174"></span><dl> <dt><strong>MIDL2174</strong></dt> </dl></td>
<td><dl> <dt><span id="attribute_expression_must_be_of_type_integer__char__Boolean_or_enum"></span><span id="attribute_expression_must_be_of_type_integer__char__boolean_or_enum"></span><span id="ATTRIBUTE_EXPRESSION_MUST_BE_OF_TYPE_INTEGER__CHAR__BOOLEAN_OR_ENUM"></span>L'espressione dell'attributo deve essere di tipo integer, char, booleano o enum</dt> <dd> Il tipo specificato non viene risolto in un tipo di commutatore valido. Usare un tipo integer, character, <a href="byte.md"><strong>byte</strong></a>, <a href="boolean.md"><strong>Boolean</strong></a>o <a href="enum.md"><strong>enum</strong></a> o un tipo derivato da uno di questi tipi.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2175"></span><span id="midl2175"></span><dl> <dt><strong>MIDL2175</strong></dt> </dl></td>
<td><dl> <dt><span id="illegal_constant"></span><span id="ILLEGAL_CONSTANT"></span>costante non valida</dt> <dd> La costante specificata non è compreso nell'intervallo valido per il tipo specificato.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2176"></span><span id="midl2176"></span><dl> <dt><strong>MIDL2176</strong></dt> </dl></td>
<td><dl> <dt><span id="attribute_not_implemented__ignored"></span><span id="ATTRIBUTE_NOT_IMPLEMENTED__IGNORED"></span>attributo non implementato; Ignorato</dt> <dd> L'attributo specificato non è implementato in questa versione di Microsoft RPC. Il compilatore MIDL continua a elaborare il file IDL come se l'attributo non fosse presente.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2177"></span><span id="midl2177"></span><dl> <dt><strong>MIDL2177</strong></dt> </dl></td>
<td><dl> <dt><span id="return_type_must_not_derive_from_a__ref__pointer"></span><span id="RETURN_TYPE_MUST_NOT_DERIVE_FROM_A__REF__POINTER"></span>il tipo restituito non deve derivare da un puntatore [ref]</dt> <dd> I valori restituiti dalla funzione definiti come tipi puntatore devono essere specificati come [<a href="unique.md"><strong>unique</strong></a>] o <a href="ptr.md"><strong>puntatori</strong></a> completi. Non è possibile usare puntatori di riferimento.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2178"></span><span id="midl2178"></span><dl> <dt><strong>MIDL2178</strong></dt> </dl></td>
<td><dl> <dt><span id="attribute_expression_must_be_a_variable_name_or_a_pointer_dereference_expression_in_this_mode._You_must_specify_the__ms_ext_switch"></span><span id="attribute_expression_must_be_a_variable_name_or_a_pointer_dereference_expression_in_this_mode._you_must_specify_the__ms_ext_switch"></span><span id="ATTRIBUTE_EXPRESSION_MUST_BE_A_VARIABLE_NAME_OR_A_POINTER_DEREFERENCE_EXPRESSION_IN_THIS_MODE._YOU_MUST_SPECIFY_THE__MS_EXT_SWITCH"></span>L'espressione dell'attributo deve essere un nome di variabile o un'espressione di dereferenziazione del puntatore in questa modalità. È necessario specificare l'opzione /ms_ext</dt> <dd> Il compilatore IDL DCE richiede che le dimensioni associate<a href="size-is.md"><strong>all'attributo</strong></a>[ size_is ] siano specificate da una variabile o da una variabile puntatore. Se si vuole sfruttare l'estensione Microsoft che consente all'attributo [<strong>size_is</strong>] di essere definito da un'espressione costante, non è possibile usare l'opzione del compilatore <a href="-osf.md"><strong>/osf.</strong></a><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2179"></span><span id="midl2179"></span><dl> <dt><strong>MIDL2179</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_must_not_derive_from_a_recursive_nonencapsulated_union"></span><span id="PARAMETER_MUST_NOT_DERIVE_FROM_A_RECURSIVE_NONENCAPSULATED_UNION"></span>il parametro non deve derivare da un'unione ricorsiva non incapsulata</dt> <dd> Un'unione deve includere una discriminante, quindi un'unione non può avere un'altra unione come elemento. Un'unione può essere incorporata in un'altra unione solo quando fa parte di una struttura che include il discriminante.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2180"></span><span id="midl2180"></span><dl> <dt><strong>MIDL2180</strong></dt> </dl></td>
<td><dl> <dt><span id="binding-handle_parameter_cannot_be__out__only"></span><span id="BINDING-HANDLE_PARAMETER_CANNOT_BE__OUT__ONLY"></span>il parametro binding-handle non può essere solo [out]</dt> <dd> Il parametro handle identificato dal compilatore MIDL come handle di associazione per questa operazione deve essere un parametro [<a href="in.md"><strong>in</strong></a>]. I parametri solo [<a href="out-idl.md"><strong>out</strong></a>] non sono definiti sullo stub del client e l'handle di associazione deve essere definito nel client.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2181"></span><span id="midl2181"></span><dl> <dt><strong>MIDL2181</strong></dt> </dl></td>
<td><dl> <dt><span id="pointer_to_a_handle_cannot_be__unique__or__ptr_"></span><span id="POINTER_TO_A_HANDLE_CANNOT_BE__UNIQUE__OR__PTR_"></span>Il puntatore a un handle non può essere [univoco] o [ptr]</dt> <dd> Non è possibile usare gli attributi univoci e completi del puntatore per un puntatore a un handle. Questi attributi consentono il valore <strong>NULL e</strong>l'handle di associazione non può essere <strong>NULL.</strong> Usare l'attributo [<a href="ref.md"><strong>ref</strong></a>] per derivare il parametro dell'handle di associazione dai puntatori di riferimento.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2182"></span><span id="midl2182"></span><dl> <dt><strong>MIDL2182</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_that_is_not_a_binding_handle_must_not_derive_from_handle_t"></span><span id="PARAMETER_THAT_IS_NOT_A_BINDING_HANDLE_MUST_NOT_DERIVE_FROM_HANDLE_T"></span>Il parametro che non è un handle di associazione non deve derivare da handle_t</dt> <dd> Il tipo di handle <a href="handle-t.md"><strong>primitivo handle_t</strong></a> non è un tipo di dati valido trasmesso in rete. Modificare il tipo di parametro in un tipo <strong>diverso handle_t</strong>o rimuovere il parametro .<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2183"></span><span id="midl2183"></span><dl> <dt><strong>MIDL2183</strong></dt> </dl></td>
<td><dl> <dt><span id="unexpected_end_of_file_found"></span><span id="UNEXPECTED_END_OF_FILE_FOUND"></span>Trovata fine imprevista del file</dt> <dd> Il compilatore MIDL ha trovato la fine del file prima di poter risolvere correttamente tutti gli elementi sintattici del file. Verificare che il carattere di terminazione della parentesi graffa destra (}) sia presente alla fine del file oppure controllare la sintassi.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2184"></span><span id="midl2184"></span><dl> <dt><strong>MIDL2184</strong></dt> </dl></td>
<td><dl> <dt><span id="type_deriving_from_handle_t_must_not_have__transmit_as__applied_to_it"></span><span id="TYPE_DERIVING_FROM_HANDLE_T_MUST_NOT_HAVE__TRANSMIT_AS__APPLIED_TO_IT"></span>Al tipo che deriva da handle_t non deve essere applicato [transmit_as]</dt> <dd> Il tipo di handle <a href="handle-t.md"><strong>primitivo handle_t</strong></a> non viene trasmesso in rete.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2185"></span><span id="midl2185"></span><dl> <dt><strong>MIDL2185</strong></dt> </dl></td>
<td><dl> <dt><span id="_context_handle__must_not_be_applied_to_a_type_that_has__handle__applied_to_it"></span><span id="_CONTEXT_HANDLE__MUST_NOT_BE_APPLIED_TO_A_TYPE_THAT_HAS__HANDLE__APPLIED_TO_IT"></span>[context_handle] non deve essere applicato a un tipo a cui è applicato [handle]</dt> <dd> Gli attributi [<a href="context-handle.md"><strong>context_handle</strong></a>] e [<a href="handle.md"><strong>handle</strong></a>] non possono essere applicati allo stesso tipo.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2186"></span><span id="midl2186"></span><dl> <dt><strong>MIDL2186</strong></dt> </dl></td>
<td><dl> <dt><span id="_handle__must_not_be_specified_on_a_type_deriving_from_void_or_void__"></span><span id="_HANDLE__MUST_NOT_BE_SPECIFIED_ON_A_TYPE_DERIVING_FROM_VOID_OR_VOID__"></span>[handle] non deve essere specificato su un tipo derivante da void o void *</dt> <dd> Un tipo specificato con l'attributo [<a href="handle.md"><strong>handle</strong></a>] può essere trasmesso in rete, ma il tipo <strong>void*</strong> non è un tipo trasmissibile. Il tipo di handle deve essere risolto in un tipo che deriva dai tipi di base trasmissibili.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2187"></span><span id="midl2187"></span><dl> <dt><strong>MIDL2187</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_must_have_either__in____out__or__in_out__in_this_mode._You_must_specify__ms_ext_or__c_ext"></span><span id="parameter_must_have_either__in____out__or__in_out__in_this_mode._you_must_specify__ms_ext_or__c_ext"></span><span id="PARAMETER_MUST_HAVE_EITHER__IN____OUT__OR__IN_OUT__IN_THIS_MODE._YOU_MUST_SPECIFY__MS_EXT_OR__C_EXT"></span>Il parametro deve avere [in], [out] o [in,out] in questa modalità. È necessario specificare /ms_ext o /c_ext</dt> <dd> Il compilatore IDL DCE richiede che tutti i parametri abbia parametri direzionali espliciti. Per usare le estensioni Microsoft per DCE IDL, non è possibile usare l'opzione <a href="-osf.md"><strong>/osf,</strong></a> che esegue l'override di <a href="-ms-ext.md"><strong>/ms_ext</strong></a> <a href="-c-ext.md"><strong>e /c_ext</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2188"></span><span id="midl2188"></span><dl> <dt><strong>MIDL2188</strong></dt> </dl></td>
<td><dl> <dt><span id="transmitted_type_may_not_derive_from__void__for__transmit_as____represent_as____wire_marshal____user_marshal_"></span><span id="TRANSMITTED_TYPE_MAY_NOT_DERIVE_FROM__VOID__FOR__TRANSMIT_AS____REPRESENT_AS____WIRE_MARSHAL____USER_MARSHAL_"></span>il tipo trasmesso non può derivare da void per &quot; &quot; [transmit_as], [represent_as], [wire_marshal], [user_marshal]</dt> <dd> <a href="transmit-as.md"><strong>L'attributo</strong></a>[ transmit_as ] si applica solo ai tipi puntatore. Usare il tipo <strong>void*</strong> al posto di <a href="void.md"><strong>void</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2189"></span><span id="midl2189"></span><dl> <dt><strong>MIDL2189</strong></dt> </dl></td>
<td><dl> <dt><span id="_void__must_be_specified_on_the_first_and_only_parameter_specification"></span><span id="_VOID__MUST_BE_SPECIFIED_ON_THE_FIRST_AND_ONLY_PARAMETER_SPECIFICATION"></span>&quot;void &quot; deve essere specificato nella specifica del primo e unico parametro</dt> <dd> La parola chiave <a href="void.md"><strong>void viene</strong></a> visualizzata in modo non corretto con altri parametri di funzione. Per specificare una funzione senza parametri, la parola chiave <strong>void</strong> deve essere l'unico elemento dell'elenco di parametri, come nell'esempio seguente:<br/>
<pre class="syntax" data-space="preserve"><code>void Moo(void)</code></pre>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2190"></span><span id="midl2190"></span><dl> <dt><strong>MIDL2190</strong></dt> </dl></td>
<td><dl> <dt><span id="_switch_is__must_be_specified_only_on_a_type_deriving_from_a_nonencapsulated_union"></span><span id="_SWITCH_IS__MUST_BE_SPECIFIED_ONLY_ON_A_TYPE_DERIVING_FROM_A_NONENCAPSULATED_UNION"></span>[switch_is] deve essere specificato solo su un tipo che deriva da un'unione non incapsulata</dt> <dd> La parola chiave [<a href="switch-is.md"><strong>switch_is</strong></a>] non è applicata correttamente. Può essere usato solo con <a href="nonencapsulated-unions.md">tipi di unione non incapsulati</a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2191"></span><span id="midl2191"></span><dl> <dt><strong>MIDL2191</strong></dt> </dl></td>
<td><dl> <dt><span id="stringable_structures_are_not_implemented_in_this_version"></span><span id="STRINGABLE_STRUCTURES_ARE_NOT_IMPLEMENTED_IN_THIS_VERSION"></span>Le strutture stringable non sono implementate in questa versione</dt> <dd> DCE IDL consente l'applicazione dell'attributo [<a href="string.md"><strong>string</strong></a>] a una struttura i cui elementi sono costituiti solo da caratteri, byte o tipi che si risolvono in caratteri o byte. Questa funzionalità non è supportata in Microsoft RPC. <strong>L'attributo</strong>[ string ] non può essere applicato all'intera struttura. Tuttavia, può essere applicato a ogni singola matrice.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2192"></span><span id="midl2192"></span><dl> <dt><strong>MIDL2192</strong></dt> </dl></td>
<td><dl> <dt><span id="switch_type_can_only_be_integral__char__Boolean_or_enum"></span><span id="switch_type_can_only_be_integral__char__boolean_or_enum"></span><span id="SWITCH_TYPE_CAN_ONLY_BE_INTEGRAL__CHAR__BOOLEAN_OR_ENUM"></span>il tipo switch può essere solo integrale, char, booleano o enum</dt> <dd> Il tipo specificato non viene risolto in un tipo di opzione valido. Usare un tipo integer, character, <a href="byte.md"><strong>byte</strong></a>, <a href="boolean.md"><strong>Boolean</strong></a>, <a href="enum.md"><strong>enum</strong></a> o un tipo derivato da uno di questi tipi.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2193"></span><span id="midl2193"></span><dl> <dt><strong>MIDL2193</strong></dt> </dl></td>
<td><dl> <dt><span id="_handle__must_not_be_specified_on_a_type_deriving_from_handle_t"></span><span id="_HANDLE__MUST_NOT_BE_SPECIFIED_ON_A_TYPE_DERIVING_FROM_HANDLE_T"></span>[handle] non deve essere specificato su un tipo che deriva da handle_t</dt> <dd> Un tipo di handle deve essere definito utilizzando uno e solo uno dei tipi di handle o degli attributi. Usare il tipo primitivo <a href="handle-t.md"><strong>handle_t</strong></a> o l'attributo [<a href="handle.md"><strong>handle</strong></a>], ma non entrambi. Il tipo di handle definito dall'utente deve essere trasmissibile, ma il <strong>tipo</strong> handle_t non viene trasmesso in rete.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2194"></span><span id="midl2194"></span><dl> <dt><strong>MIDL2194</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_deriving_from_handle_t_must_not_be_an__out__parameter"></span><span id="PARAMETER_DERIVING_FROM_HANDLE_T_MUST_NOT_BE_AN__OUT__PARAMETER"></span>il parametro che deriva da handle_t non deve essere un parametro [out]</dt> <dd> Un handle del tipo primitivo <a href="handle-t.md"><strong>handle_t</strong></a> è significativo solo per il lato dell'applicazione in cui è definito. Il <strong>tipo handle_t</strong> non viene trasmesso in rete.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2195"></span><span id="midl2195"></span><dl> <dt><strong>MIDL2195</strong></dt> </dl></td>
<td><dl> <dt><span id="attribute_expression_derives_from__unique__or__ptr__pointer_dereference"></span><span id="ATTRIBUTE_EXPRESSION_DERIVES_FROM__UNIQUE__OR__PTR__POINTER_DEREFERENCE"></span>L'espressione attribute deriva dalla dereferenziazione del puntatore [unique] o [ptr]</dt> <dd> Anche se gli attributi [<a href="unique.md"><strong>unique</strong></a>] e <a href="ptr.md"><strong>full</strong></a> pointer consentono ai puntatori di avere valori <strong>NULL,</strong> l'espressione che definisce l'attributo size o length non deve mai avere <strong>un valore NULL.</strong> Quando vengono usati i puntatori, MIDL vincola le espressioni ai puntatori [<a href="ref.md"><strong>ref</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2196"></span><span id="midl2196"></span><dl> <dt><strong>MIDL2196</strong></dt> </dl></td>
<td><dl> <dt><span id="_cpp_quote__requires__ms_ext"></span><span id="_CPP_QUOTE__REQUIRES__MS_EXT"></span>&quot;cpp_quote &quot; richiede /ms_ext</dt> <dd> <a href="cpp-quote.md"><strong>L cpp_quote</strong></a> attributo è un'estensione Microsoft di DCE IDL. Non usare l'opzione del compilatore MIDL <a href="-osf.md"><strong>/osf</strong></a>, che esegue l'override <a href="-ms-ext.md"><strong>di /ms_ext</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2197"></span><span id="midl2197"></span><dl> <dt><strong>MIDL2197</strong></dt> </dl></td>
<td><dl> <dt><span id="quoted_uuid_requires__ms_ext"></span><span id="QUOTED_UUID_REQUIRES__MS_EXT"></span>quoted uuid richiede /ms_ext</dt> <dd> La possibilità di specificare un valore UUID tra virgolette è un'estensione Microsoft di DCE IDL. Non usare l'opzione del compilatore MIDL <a href="-osf.md"><strong>/osf</strong></a>, che esegue l'override <a href="-ms-ext.md"><strong>di /ms_ext</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2198"></span><span id="midl2198"></span><dl> <dt><strong>MIDL2198</strong></dt> </dl></td>
<td><dl> <dt><span id="return_type_cannot_derive_from_a_nonencapsulated_union"></span><span id="RETURN_TYPE_CANNOT_DERIVE_FROM_A_NONENCAPSULATED_UNION"></span>Il tipo restituito non può derivare da un'unione non incapsulata</dt> <dd> L'unione non incapsulata non può essere usata come tipo restituito dalla funzione. Per restituire il tipo di unione, specificare il tipo di unione come parametro [<a href="out-idl.md"><strong>out</strong></a>] o [<strong>in, out</strong>].<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2199"></span><span id="midl2199"></span><dl> <dt><strong>MIDL2199</strong></dt> </dl></td>
<td><dl> <dt><span id="return_type_cannot_derive_from_a_conformant_structure"></span><span id="RETURN_TYPE_CANNOT_DERIVE_FROM_A_CONFORMANT_STRUCTURE"></span>Il tipo restituito non può derivare da una struttura conforme</dt> <dd> La dimensione del tipo restituito deve essere una costante. Non è possibile specificare come tipo restituito una struttura che contiene una matrice conforme anche quando la struttura include anche il relativo identificatore di dimensioni. Per restituire la struttura conforme, specificare la struttura come parametro [<a href="out-idl.md"><strong>out</strong></a>] o [<strong>in, out</strong>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2200"></span><span id="midl2200"></span><dl> <dt><strong>MIDL2200</strong></dt> </dl></td>
<td><dl> <dt><span id="_transmit_as__must_not_be_applied_to_a_type_deriving_from_a_generic_handle"></span><span id="_TRANSMIT_AS__MUST_NOT_BE_APPLIED_TO_A_TYPE_DERIVING_FROM_A_GENERIC_HANDLE"></span>[transmit_as] non deve essere applicato a un tipo che deriva da un handle generico</dt> <dd> In questa versione gli attributi [<a href="handle.md"><strong>handle</strong></a>] e [<a href="transmit-as.md"><strong>transmit_as</strong></a>] non possono essere combinati nello stesso tipo.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2201"></span><span id="midl2201"></span><dl> <dt><strong>MIDL2201</strong></dt> </dl></td>
<td><dl> <dt><span id="_handle__must_not_be_applied_to_a_type_that_has__transmit_as__applied_to_it"></span><span id="_HANDLE__MUST_NOT_BE_APPLIED_TO_A_TYPE_THAT_HAS__TRANSMIT_AS__APPLIED_TO_IT"></span>[handle] non deve essere applicato a un tipo a cui è applicato [transmit_as]</dt> <dd> In questa versione gli attributi [<a href="handle.md"><strong>handle</strong></a>] e [<a href="transmit-as.md"><strong>transmit_as</strong></a>] non possono essere combinati nello stesso tipo.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2202"></span><span id="midl2202"></span><dl> <dt><strong>MIDL2202</strong></dt> </dl></td>
<td><dl> <dt><span id="type_specified_for_the_const_declaration_is_invalid"></span><span id="TYPE_SPECIFIED_FOR_THE_CONST_DECLARATION_IS_INVALID"></span>Il tipo specificato per la dichiarazione const non è valido</dt> <dd> Le dichiarazioni di costanti sono limitate ai tipi Integer, Character, Wide Character, String e Boolean.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2203"></span><span id="midl2203"></span><dl> <dt><strong>MIDL2203</strong></dt> </dl></td>
<td><dl> <dt><span id="operand_to_the_sizeof_operator_is_not_supported"></span><span id="OPERAND_TO_THE_SIZEOF_OPERATOR_IS_NOT_SUPPORTED"></span>L'operando per l'operatore sizeof non è supportato</dt> <dd> Il compilatore MIDL supporta <strong>l'operazione sizeof</strong> solo per i tipi semplici. L'operando specificato non restituisce un tipo Integer.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2204"></span><span id="midl2204"></span><dl> <dt><strong>MIDL2204</strong></dt> </dl></td>
<td><dl> <dt><span id="this_name_already_used_as_a_const_identifier_name"></span><span id="THIS_NAME_ALREADY_USED_AS_A_CONST_IDENTIFIER_NAME"></span>questo nome è già usato come nome di identificatore const</dt> <dd> L'identificatore è stato usato in precedenza per identificare una costante in una <a href="const.md"><strong>dichiarazione const.</strong></a> Modificare il nome di uno degli identificatori in modo che gli identificatori siano univoci.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2205"></span><span id="midl2205"></span><dl> <dt><strong>MIDL2205</strong></dt> </dl></td>
<td><dl> <dt><span id="inconsistent_redefinition_of_type_error_status_t"></span><span id="INCONSISTENT_REDEFINITION_OF_TYPE_ERROR_STATUS_T"></span>ridefinizione incoerente del tipo error_status_t</dt> <dd> Il tipo <a href="error-status-t.md"><strong>error_status_t</strong></a> deve risolversi nel tipo <strong>unsigned long</strong>. Non è possibile usare altre definizioni di tipo.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2206"></span><span id="midl2206"></span><dl> <dt><strong>MIDL2206</strong></dt> </dl></td>
<td><dl> <dt><span id="_case__value_out_of_range_of_switch_type"></span><span id="_CASE__VALUE_OUT_OF_RANGE_OF_SWITCH_TYPE"></span>[case] valore non compreso nell'intervallo del tipo switch</dt> <dd> Il valore associato al case dell'istruzione switch non è compreso nell'intervallo per il tipo switch specificato. Ad esempio, questo errore si verifica quando nell'istruzione case long integer un valore di tipo short integer.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2207"></span><span id="midl2207"></span><dl> <dt><strong>MIDL2207</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_deriving_from_wchar_t_needs__ms_ext"></span><span id="PARAMETER_DERIVING_FROM_WCHAR_T_NEEDS__MS_EXT"></span>il parametro che deriva da wchar_t richiede /ms_ext</dt> <dd> Il tipo di carattere <a href="wchar-t.md"><strong>wide wchar_t</strong></a> è un'estensione Microsoft di DCE IDL. Non usare l'opzione del compilatore MIDL <a href="-osf.md"><strong>/osf</strong></a>, che esegue l'override <a href="-ms-ext.md"><strong>di /ms_ext</strong></a><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2208"></span><span id="midl2208"></span><dl> <dt><strong>MIDL2208</strong></dt> </dl></td>
<td><dl> <dt><span id="this_interface_has_only_callbacks"></span><span id="THIS_INTERFACE_HAS_ONLY_CALLBACKS"></span>questa interfaccia ha solo callback</dt> <dd> I callback sono validi solo nel contesto di una chiamata di procedura remota. L'interfaccia deve includere almeno un prototipo di funzione per una chiamata di procedura remota che non include l'attributo [<a href="callback.md"><strong>callback</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2209"></span><span id="midl2209"></span><dl> <dt><strong>MIDL2209</strong></dt> </dl></td>
<td><dl> <dt><span id="redundantly_specified_attribute__ignored"></span><span id="REDUNDANTLY_SPECIFIED_ATTRIBUTE__IGNORED"></span>attributo specificato in modo ridondante; Ignorato</dt> <dd> L'attributo specificato è stato applicato più di una volta. Più istanze dello stesso attributo vengono ignorate.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2210"></span><span id="midl2210"></span><dl> <dt><strong>MIDL2210</strong></dt> </dl></td>
<td><dl> <dt><span id="context_handle_type_used_for_an_implicit_handle"></span><span id="CONTEXT_HANDLE_TYPE_USED_FOR_AN_IMPLICIT_HANDLE"></span>Tipo di handle di contesto usato per un handle implicito</dt> <dd> È stato specificato un tipo definito usando l'attributo [<a href="context-handle.md"><strong>context_handle</strong></a>] come tipo di handle in un attributo [ <a href="implicit-handle.md"><strong>implicit_handle</strong></a>]. Gli attributi non possono essere combinati in questo modo.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2211"></span><span id="midl2211"></span><dl> <dt><strong>MIDL2211</strong></dt> </dl></td>
<td><dl> <dt><span id="conflicting_options_specified_for__allocate_"></span><span id="CONFLICTING_OPTIONS_SPECIFIED_FOR__ALLOCATE_"></span>opzioni in conflitto specificate per [allocare]</dt> <dd> Le opzioni specificate per l'attributo ACF [<a href="allocate.md"><strong>allocate</strong></a>] rappresentano direttive in conflitto. Ad esempio, specificare l'opzione all_nodes o l'opzione single_node, ma non entrambe.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2212"></span><span id="midl2212"></span><dl> <dt><strong>MIDL2212</strong></dt> </dl></td>
<td><dl> <dt><span id="error_while_writing_to_file"></span><span id="ERROR_WHILE_WRITING_TO_FILE"></span>errore durante la scrittura nel file</dt> <dd> Si è verificato un errore durante la scrittura nel file. Questa condizione può essere causata da errori relativi allo spazio su disco, agli handle di file, alle restrizioni di accesso ai file e agli errori hardware.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2213"></span><span id="midl2213"></span><dl> <dt><strong>MIDL2213</strong></dt> </dl></td>
<td><dl> <dt><span id="no_switch_type_found_at_definition_of_union__using_the__switch_is__type"></span><span id="NO_SWITCH_TYPE_FOUND_AT_DEFINITION_OF_UNION__USING_THE__SWITCH_IS__TYPE"></span>nessun tipo switch trovato nella definizione di union, usando il tipo [switch_is]</dt> <dd> La definizione di unione non include un attributo [<a href="switch-type.md"><strong>switch_type</strong></a>] esplicito. Il tipo della variabile specificata<a href="switch-is.md"><strong>dall'attributo</strong></a>[ switch_is ] viene usato come tipo di opzione.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2214"></span><span id="midl2214"></span><dl> <dt><strong>MIDL2214</strong></dt> </dl></td>
<td><dl> <dt><span id="semantic_check_incomplete_due_to_previous_errors"></span><span id="SEMANTIC_CHECK_INCOMPLETE_DUE_TO_PREVIOUS_ERRORS"></span>controllo semantico incompleto a causa di errori precedenti</dt> <dd> Il compilatore MIDL esegue due passaggi sui file di input per risolvere eventuali dichiarazioni con inoltro. A causa di errori rilevati durante il primo passaggio, non è stato eseguito il controllo del secondo passaggio. È possibile che nel file siano ancora presenti errori non generati relativi alle dichiarazioni con inoltro.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2215"></span><span id="midl2215"></span><dl> <dt><strong>MIDL2215</strong></dt> </dl></td>
<td><dl> <dt><span id="handle_parameter_or_return_type_is_not_supported_on_a__callback__procedure"></span><span id="HANDLE_PARAMETER_OR_RETURN_TYPE_IS_NOT_SUPPORTED_ON_A__CALLBACK__PROCEDURE"></span>Il parametro handle o il tipo restituito non è supportato in una routine [callback]</dt> <dd> Una routine [<a href="callback.md"><strong>callback</strong></a>] si verifica nel contesto di una chiamata da un client al server e usa lo stesso handle di associazione della chiamata originale. I parametri di handle di associazione espliciti o i tipi restituiti non sono consentiti nelle funzioni di callback.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2216"></span><span id="midl2216"></span><dl> <dt><strong>MIDL2216</strong></dt> </dl></td>
<td><dl> <dt><span id="_ptr__does_not_support_aliasing_in_this_version"></span><span id="_PTR__DOES_NOT_SUPPORT_ALIASING_IN_THIS_VERSION"></span>[ptr] non supporta l'aliasing in questa versione</dt> <dd> Un alias si verifica quando i dati sono accessibili tramite più di un puntatore o un nome di variabile. Rimuovere l'alias. Per altre informazioni, vedere <a href="/windows/desktop/Rpc/unique-pointers">Puntatori univoci.</a><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2217"></span><span id="midl2217"></span><dl> <dt><strong>MIDL2217</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_already_defined_as_a_context_handle"></span><span id="PARAMETER_ALREADY_DEFINED_AS_A_CONTEXT_HANDLE"></span>parametro già definito come handle di contesto</dt> <dd> Il parametro è stato definito in precedenza come handle di contesto.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2218"></span><span id="midl2218"></span><dl> <dt><strong>MIDL2218</strong></dt> </dl></td>
<td><dl> <dt><span id="_context_handle__must_not_derive_from_handle_t"></span><span id="_CONTEXT_HANDLE__MUST_NOT_DERIVE_FROM_HANDLE_T"></span>[context_handle] non deve derivare da handle_t</dt> <dd> Le tre caratteristiche dell'handle: il <a href="handle-t.md"><strong>tipo handle_t</strong></a>, l'attributo [<a href="handle.md"><strong>handle</strong></a>] e l'attributo [<a href="context-handle.md"><strong>context_handle</strong></a>], si escludono a vicenda. È possibile applicare una sola caratteristica a un tipo o a un parametro alla volta.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2219"></span><span id="midl2219"></span><dl> <dt><strong>MIDL2219</strong></dt> </dl></td>
<td><dl> <dt><span id="array_size_exceeds_65536_bytes"></span><span id="ARRAY_SIZE_EXCEEDS_65536_BYTES"></span>le dimensioni della matrice superano i 65536 byte</dt> <dd> In alcune piattaforme Microsoft, la dimensione massima trasmissibile dei dati è 64K. Riprogettare l'applicazione in modo che tutti i dati trasmessi si adattino alle dimensioni massime trasmissibili.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2220"></span><span id="midl2220"></span><dl> <dt><strong>MIDL2220</strong></dt> </dl></td>
<td><dl> <dt><span id="structure_size_exceeds_65536_bytes"></span><span id="STRUCTURE_SIZE_EXCEEDS_65536_BYTES"></span>le dimensioni della struttura superano i 65536 byte</dt> <dd> In alcune piattaforme Microsoft, la dimensione massima trasmissibile dei dati è 64K. Riprogettare l'applicazione in modo che tutti i dati trasmessi si adattino alle dimensioni massime trasmissibili.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2221"></span><span id="midl2221"></span><dl> <dt><strong>MIDL2221</strong></dt> </dl></td>
<td><dl> <dt><span id="field_of_a_nonencapsulated_union_cannot_be_another_nonencapsulated_union"></span><span id="FIELD_OF_A_NONENCAPSULATED_UNION_CANNOT_BE_ANOTHER_NONENCAPSULATED_UNION"></span>Il campo di un'unione non incapsulata non può essere un'altra unione non incapsulata</dt> <dd> Le unioni trasmesse come parte di una chiamata di procedura remota richiedono un elemento dati associato, il discriminante, che seleziona il arm di unione. Le unioni annidate in altre unioni non offrono una discriminante; di conseguenza, non possono essere trasmessi in questo formato. Creare una struttura costituita dall'unione e dalla relativa discriminante.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2222"></span><span id="midl2222"></span><dl> <dt><strong>MIDL2222</strong></dt> </dl></td>
<td><dl> <dt><span id="pointer_attribute_s__applied_on_an_embedded_array__ignored"></span><span id="POINTER_ATTRIBUTE_S__APPLIED_ON_AN_EMBEDDED_ARRAY__IGNORED"></span>attributi puntatore applicati a una matrice incorporata; Ignorato</dt> <dd> Un attributo puntatore può essere applicato a una matrice solo quando la matrice è un parametro di primo livello. Gli altri attributi del puntatore applicati alle matrici incorporate in altre strutture di dati vengono ignorati.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2223"></span><span id="midl2223"></span><dl> <dt><strong>MIDL2223</strong></dt> </dl></td>
<td><dl> <dt><span id="_allocate__is_illegal_on_either_the_transmitted_or_presented_type_for__transmit_as____represent_as____wire_marshal___or__user_marshal_"></span><span id="_ALLOCATE__IS_ILLEGAL_ON_EITHER_THE_TRANSMITTED_OR_PRESENTED_TYPE_FOR__TRANSMIT_AS____REPRESENT_AS____WIRE_MARSHAL___OR__USER_MARSHAL_"></span>[allocate] non è valido nel tipo trasmesso o presentato per [transmit_as], [represent_as], [wire_marshal] o [user_marshal]</dt> <dd> Gli attributi [<a href="transmit-as.md"><strong>transmit_as</strong></a>] e [<a href="allocate.md"><strong>allocate</strong></a>] non possono essere applicati entrambi allo stesso tipo. <strong>L'attributo</strong>[ transmit_as ] distingue tra i tipi presentati e trasmessi, mentre l'attributo [<strong>allocate</strong>] presuppone che il tipo presentato sia lo stesso del tipo trasmesso.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2224"></span><span id="midl2224"></span><dl> <dt><strong>MIDL2224</strong></dt> </dl></td>
<td>[switch_type] deve essere specificato in questa modalità di importazione<br/></td>
</tr>
<tr class="even">
<td><span id="MIDL2225"></span><span id="midl2225"></span><dl> <dt><strong>MIDL2225</strong></dt> </dl></td>
<td><dl> <dt><span id="_implicit_handle__type_undefined__assuming_generic_handle"></span><span id="_IMPLICIT_HANDLE__TYPE_UNDEFINED__ASSUMING_GENERIC_HANDLE"></span>[implicit_handle] tipo non definito; presupponendo un handle generico</dt> <dd> Il tipo di handle specificato in ACF non è definito nel file IDL. Il compilatore MIDL presuppone che il tipo di handle si risolva nel tipo di handle primitivo <a href="handle-t.md"><strong>handle_t</strong></a>. Aggiungere<a href="handle.md"><strong>l'attributo</strong></a>[ handle ] alla definizione del tipo se si vuole che l'handle si comporti come un handle definito dall'utente o generico.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2226"></span><span id="midl2226"></span><dl> <dt><strong>MIDL2226</strong></dt> </dl></td>
<td><dl> <dt><span id="array_element_must_not_derive_from_error_status_t"></span><span id="ARRAY_ELEMENT_MUST_NOT_DERIVE_FROM_ERROR_STATUS_T"></span>L'elemento array non deve derivare da error_status_t</dt> <dd> In questa versione di Microsoft RPC, il tipo <a href="error-status-t.md"><strong>error_status_t</strong></a> può essere visualizzato solo come parametro o tipo restituito. Non può essere visualizzato nelle matrici.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2227"></span><span id="midl2227"></span><dl> <dt><strong>MIDL2227</strong></dt> </dl></td>
<td><dl> <dt><span id="_allocate__illegal_on_a_type_deriving_from_a_primitive_generic_context_handle"></span><span id="_ALLOCATE__ILLEGAL_ON_A_TYPE_DERIVING_FROM_A_PRIMITIVE_GENERIC_CONTEXT_HANDLE"></span>[allocate] non valido in un tipo che deriva da un handle primitivo/generico/di contesto</dt> <dd> Per impostazione predefinita, l'attributo ACF [<a href="allocate.md"><strong>allocate</strong></a>] non può essere applicato ai tipi di handle.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2228"></span><span id="midl2228"></span><dl> <dt><strong>MIDL2228</strong></dt> </dl></td>
<td><dl> <dt><span id="transmitted_or_presented_type_must_not_derive_from_error_status_t"></span><span id="TRANSMITTED_OR_PRESENTED_TYPE_MUST_NOT_DERIVE_FROM_ERROR_STATUS_T"></span>Il tipo trasmesso o presentato non deve derivare da error_status_t</dt> <dd> In questa versione di Microsoft RPC, il <a href="error-status-t.md"><strong>tipo error_status_t</strong></a> non può essere usato con l'attributo [<a href="transmit-as.md"><strong>transmit_as</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2229"></span><span id="midl2229"></span><dl> <dt><strong>MIDL2229</strong></dt> </dl></td>
<td><dl> <dt><span id="discriminant_of_a_union_must_not_derive_from_a_field_with__ignore__applied_to_it"></span><span id="DISCRIMINANT_OF_A_UNION_MUST_NOT_DERIVE_FROM_A_FIELD_WITH__IGNORE__APPLIED_TO_IT"></span>la discriminante di un'unione non deve derivare da un campo a cui è applicato [ignore]</dt> <dd> Un'unione utilizzata in una chiamata di procedura remota deve essere associata a un altro elemento di dati, denominato discriminante, che seleziona il arm di unione. Il discriminante deve essere trasmesso. <a href="ignore.md"><strong>L'attributo</strong></a>[ ignore ] non può essere applicato alla discriminante dell'unione.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2230"></span><span id="midl2230"></span><dl> <dt><strong>MIDL2230</strong></dt> </dl></td>
<td><dl> <dt><span id="_nocode__ignored_for_server_side_since___server_none__not_specified"></span><span id="_NOCODE__IGNORED_FOR_SERVER_SIDE_SINCE___SERVER_NONE__NOT_SPECIFIED"></span>[nocode] ignorato per il lato server perché &quot; /server none &quot; non specificato</dt> <dd> Alcuni compilatori IDL DCE generano un errore quando l'attributo [<a href="nocode.md"><strong>nocode</strong></a>] viene applicato a una routine in un'interfaccia per cui vengono generati file stub del server. Poiché il server deve supportare tutte le operazioni, [<strong>nocode</strong>] non deve essere applicato a una routine in questa modalità oppure è necessario usare l'opzione del compilatore MIDL <a href="-server.md"><strong>/server</strong></a> none per specificare in modo esplicito che non deve essere generata alcuna routine del server.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2231"></span><span id="midl2231"></span><dl> <dt><strong>MIDL2231</strong></dt> </dl></td>
<td><dl> <dt><span id="no_remote_procedures_specified_in_non-_local__interface__no_client_server_stubs_will_be_generated"></span><span id="NO_REMOTE_PROCEDURES_SPECIFIED_IN_NON-_LOCAL__INTERFACE__NO_CLIENT_SERVER_STUBS_WILL_BE_GENERATED"></span>nessuna routine remota specificata nell'interfaccia non[local]. non verranno generati stub client/server</dt> <dd> L'interfaccia fornita non dispone di procedure remote, quindi verranno generati solo i file di intestazione.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2232"></span><span id="midl2232"></span><dl> <dt><strong>MIDL2232</strong></dt> </dl></td>
<td><dl> <dt><span id="too_many_default_cases_specified_for_encapsulated_union"></span><span id="TOO_MANY_DEFAULT_CASES_SPECIFIED_FOR_ENCAPSULATED_UNION"></span>troppi case predefiniti specificati per l'unione incapsulata</dt> <dd> Un'unione incapsulata può avere un solo valore predefinito: arm.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2233"></span><span id="midl2233"></span><dl> <dt><strong>MIDL2233</strong></dt> </dl></td>
<td><dl> <dt><span id="too_many_default_interfaces_specified_for_coclass"></span><span id="TOO_MANY_DEFAULT_INTERFACES_SPECIFIED_FOR_COCLASS"></span>troppe interfacce predefinite specificate per la coclasse</dt> <dd> Una <a href="coclass.md"><strong>coclasse</strong></a> può avere al massimo due membri [<a href="default.md"><strong>default</strong></a>], uno per rappresentare l'interfaccia in uscita (di origine) o l'interfaccia dispatch e uno per rappresentare l'interfaccia in ingresso (sink) o l'interfaccia dispatch.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2234"></span><span id="midl2234"></span><dl> <dt><strong>MIDL2234</strong></dt> </dl></td>
<td><dl> <dt><span id="items_with__defaultvtable__must_also_have__source_"></span><span id="ITEMS_WITH__DEFAULTVTABLE__MUST_ALSO_HAVE__SOURCE_"></span>Anche gli elementi con [defaultvtable] devono avere [source]</dt> <dd> <a href="defaultvtable.md"><strong>L'interfaccia defaultvtable</strong></a> crea una seconda interfaccia di origine per un oggetto, che consente ai sink di ricevere eventi tramite la tabella V.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2235"></span><span id="midl2235"></span><dl> <dt><strong>MIDL2235</strong></dt> </dl></td>
<td><dl> <dt><span id="union_specification_with_no_fields_is_illegal"></span><span id="UNION_SPECIFICATION_WITH_NO_FIELDS_IS_ILLEGAL"></span>La specifica dell'unione senza campi non è valida</dt> <dd> Le unioni devono avere almeno un campo.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2236"></span><span id="midl2236"></span><dl> <dt><strong>MIDL2236</strong></dt> </dl></td>
<td><dl> <dt><span id="value_out_of_range"></span><span id="VALUE_OUT_OF_RANGE"></span>valore non compreso nell'intervallo</dt> <dd> Il valore case fornito non è compreso nell'intervallo del tipo di opzione.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2237"></span><span id="midl2237"></span><dl> <dt><strong>MIDL2237</strong></dt> </dl></td>
<td><dl> <dt><span id="_context_handle__must_be_applied_on_a_pointer_type"></span><span id="_CONTEXT_HANDLE__MUST_BE_APPLIED_ON_A_POINTER_TYPE"></span>[context_handle] deve essere applicato a un tipo di puntatore</dt> <dd> Gli handle di contesto devono essere sempre tipi puntatore. DCE specifica che tutti gli handle di contesto devono essere tipizzati <strong>come void *</strong>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2238"></span><span id="midl2238"></span><dl> <dt><strong>MIDL2238</strong></dt> </dl></td>
<td><dl> <dt><span id="return_type_must_not_derive_from_handle_t"></span><span id="RETURN_TYPE_MUST_NOT_DERIVE_FROM_HANDLE_T"></span>Il tipo restituito non deve derivare da handle_t</dt> <dd><a href="handle-t.md"><strong>handle_t</strong></a> non può essere restituito.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2239"></span><span id="midl2239"></span><dl> <dt><strong>MIDL2239</strong></dt> </dl></td>
<td><dl> <dt><span id="_handle__must_not_be_applied_to_a_type_deriving_from_a_context_handle"></span><span id="_HANDLE__MUST_NOT_BE_APPLIED_TO_A_TYPE_DERIVING_FROM_A_CONTEXT_HANDLE"></span>[handle] non deve essere applicato a un tipo derivante da un handle di contesto</dt> <dd> Un tipo non può essere sia un handle di contesto che un handle generico.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2240"></span><span id="midl2240"></span><dl> <dt><strong>MIDL2240</strong></dt> </dl></td>
<td><dl> <dt><span id="field_deriving_from_an__int__must_have_size_specifier__small____short___or__long__with_the__int_"></span><span id="FIELD_DERIVING_FROM_AN__INT__MUST_HAVE_SIZE_SPECIFIER__SMALL____SHORT___OR__LONG__WITH_THE__INT_"></span>il campo derivante da un int deve avere l'identificatore di dimensione &quot; small , short o long &quot; con &quot; &quot; &quot; &quot; &quot; &quot; &quot; int&quot;</dt> <dd> Il tipo <a href="int.md"><strong>int</strong></a> non è trasmissibile nei sistemi a 16 bit, poiché le dimensioni di <strong>int</strong> possono essere diverse tra computer.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2241"></span><span id="midl2241"></span><dl> <dt><strong>MIDL2241</strong></dt> </dl></td>
<td><dl> <dt><span id="field_must_not_derive_from_a_void_or_void__"></span><span id="FIELD_MUST_NOT_DERIVE_FROM_A_VOID_OR_VOID__"></span>il campo non deve derivare da un void o void *</dt> <dd> <strong>void</strong> e <strong>void * non</strong> possono essere usati come tipi di parametro per le procedure remote.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2242"></span><span id="midl2242"></span><dl> <dt><strong>MIDL2242</strong></dt> </dl></td>
<td><dl> <dt><span id="field_must_not_derive_from_a_structure_containing_bit-fields"></span><span id="FIELD_MUST_NOT_DERIVE_FROM_A_STRUCTURE_CONTAINING_BIT-FIELDS"></span>il campo non deve derivare da una struttura contenente campi di bit</dt> <dd> Le strutture contenenti campi di bit non possono essere usate come parametri o tipi restituiti per le procedure remote.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2243"></span><span id="midl2243"></span><dl> <dt><strong>MIDL2243</strong></dt> </dl></td>
<td><dl> <dt><span id="field_must_not_derive_from_a_non-rpcable_union"></span><span id="FIELD_MUST_NOT_DERIVE_FROM_A_NON-RPCABLE_UNION"></span>il campo non deve derivare da un'unione non rpcable</dt> <dd> Un'unione deve essere specificata come unione non incapsulata o incapsulata per poter essere trasmessa. Le unioni C ordinarie non hanno la discriminante necessaria per trasmettere l'unione attraverso la rete.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2244"></span><span id="midl2244"></span><dl> <dt><strong>MIDL2244</strong></dt> </dl></td>
<td><dl> <dt><span id="field_must_not_derive_from_a_pointer_to_a_function"></span><span id="FIELD_MUST_NOT_DERIVE_FROM_A_POINTER_TO_A_FUNCTION"></span>il campo non deve derivare da un puntatore a una funzione</dt> <dd> I puntatori alle funzioni non possono essere trasmessi a procedure remote. I puntatori alle funzioni puntano al codice della funzione e nessun codice di funzione può essere trasmesso in rete tramite RPC.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2245"></span><span id="midl2245"></span><dl> <dt><strong>MIDL2245</strong></dt> </dl></td>
<td><dl> <dt><span id="cannot_use__fault_status__on_both_a_parameter_and_a_return_type"></span><span id="CANNOT_USE__FAULT_STATUS__ON_BOTH_A_PARAMETER_AND_A_RETURN_TYPE"></span>impossibile usare [fault_status] sia in un parametro che in un tipo restituito</dt> <dd> L'attributo [<a href="fault-status.md"><strong>fault_status</strong></a>] può essere usato una sola volta per ogni procedura. <a href="comm-status.md"><strong>L'attributo</strong></a>[ comm_status ] può essere usato in modo indipendente.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2246"></span><span id="midl2246"></span><dl> <dt><strong>MIDL2246</strong></dt> </dl></td>
<td><dl> <dt><span id="return_type_too_complicated_for__Oi_modes__using__Os"></span><span id="return_type_too_complicated_for__oi_modes__using__os"></span><span id="RETURN_TYPE_TOO_COMPLICATED_FOR__OI_MODES__USING__OS"></span>tipo restituito troppo complesso per le modalità /Oi, con /Os</dt> <dd> I tipi restituiti di grandi dimensioni passati per valore possono essere gestiti solo dagli stub <a href="-os.md"><strong>di ottimizzazione /Os.</strong></a> Gli stub per questa routine verranno generati usando <strong>l'ottimizzazione /Os.</strong><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2247"></span><span id="midl2247"></span><dl> <dt><strong>MIDL2247</strong></dt> </dl></td>
<td><dl> <dt><span id="generic_handle_type_too_large_for__Oi_modes__using__Os"></span><span id="generic_handle_type_too_large_for__oi_modes__using__os"></span><span id="GENERIC_HANDLE_TYPE_TOO_LARGE_FOR__OI_MODES__USING__OS"></span>Tipo di handle generico troppo grande per le modalità /Oi, con /Os</dt> <dd> I tipi di handle generici di grandi dimensioni passati per valore possono essere gestiti solo dagli stub <a href="-os.md"><strong>di ottimizzazione /Os.</strong></a> Gli stub per questa routine verranno generati usando <strong>l'ottimizzazione /Os.</strong><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2248"></span><span id="midl2248"></span><dl> <dt><strong>MIDL2248</strong></dt> </dl></td>
<td><dl> <dt><span id="_allocate_all_nodes___on_an__in_out__parameter_may_orphan_the_original_memory"></span><span id="_ALLOCATE_ALL_NODES___ON_AN__IN_OUT__PARAMETER_MAY_ORPHAN_THE_ORIGINAL_MEMORY"></span>[allocate(all_nodes)] in un parametro [in,out] può orfare la memoria originale</dt> <dd> L'uso di [<a href="allocate.md"><strong>allocate</strong></a>(all_nodes)] in un parametro [<a href="in.md"><strong>in</strong></a>, <a href="out-idl.md"><strong>out</strong></a>] deve riallocare la memoria contigua per la direzione [<strong>out</strong>], rendendo così orfano il parametro [<strong>in</strong>]. Questo utilizzo non è consigliato.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2249"></span><span id="midl2249"></span><dl> <dt><strong>MIDL2249</strong></dt> </dl></td>
<td><dl> <dt><span id="cannot_have_a__ref__pointer_as_a_union_arm"></span><span id="CANNOT_HAVE_A__REF__POINTER_AS_A_UNION_ARM"></span>non può avere un puntatore [ref] come arm di unione</dt> <dd> I puntatori di riferimento devono sempre puntare a una memoria valida, ma un'unione [<a href="in.md"><strong>in</strong></a>, <a href="out-idl.md"><strong>out</strong></a>] con un puntatore di riferimento può restituire un puntatore di riferimento quando la direzione [<strong>in</strong>] usa un altro tipo.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2250"></span><span id="midl2250"></span><dl> <dt><strong>MIDL2250</strong></dt> </dl></td>
<td><dl> <dt><span id="return_of_context_handles_not_supported_for__Oi_modes__using__Os"></span><span id="return_of_context_handles_not_supported_for__oi_modes__using__os"></span><span id="RETURN_OF_CONTEXT_HANDLES_NOT_SUPPORTED_FOR__OI_MODES__USING__OS"></span>restituzione di handle di contesto non supportati per le modalità /Oi, con /Os</dt> <dd> MIDL non supporta gli handle di contesto nelle modalità di ottimizzazione completamente interpretate. Passaggio all'ottimizzazione in modalità mista.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2251"></span><span id="midl2251"></span><dl> <dt><strong>MIDL2251</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of_the_extra__comm_status__or__fault_status__parameter_not_supported_for__Oi_modes__using__Os"></span><span id="use_of_the_extra__comm_status__or__fault_status__parameter_not_supported_for__oi_modes__using__os"></span><span id="USE_OF_THE_EXTRA__COMM_STATUS__OR__FAULT_STATUS__PARAMETER_NOT_SUPPORTED_FOR__OI_MODES__USING__OS"></span>Uso del parametro aggiuntivo [comm_status] o [fault_status] non supportato per le modalità /Oi, con /Os</dt> <dd> Gli attributi [<a href="comm-status.md"><strong>comm_status</strong></a>] e [<a href="fault-status.md"><strong>fault_status</strong></a>] possono essere gestiti solo dagli stub di ottimizzazione <a href="-os.md"><strong>/Os.</strong></a> Gli stub per questa routine verranno generati usando <strong>l'ottimizzazione /Os.</strong><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2252"></span><span id="midl2252"></span><dl> <dt><strong>MIDL2252</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of_an_unknown_type_for__represent_as__or__user_marshal__not_supported_for__Oi_modes__using__Os"></span><span id="use_of_an_unknown_type_for__represent_as__or__user_marshal__not_supported_for__oi_modes__using__os"></span><span id="USE_OF_AN_UNKNOWN_TYPE_FOR__REPRESENT_AS__OR__USER_MARSHAL__NOT_SUPPORTED_FOR__OI_MODES__USING__OS"></span>Uso di un tipo sconosciuto per [represent_as] o [user_marshal] non supportato per le modalità /Oi, con /Os</dt> <dd> L'uso dell'attributo [<a href="represent-as.md"><strong>represent_as</strong></a>] con un tipo locale non definito nel file IDL o un file IDL importato può essere gestito solo dagli stub di ottimizzazione <a href="-os.md"><strong>/Os.</strong></a> Gli stub per questa routine verranno generati usando <strong>l'ottimizzazione /Os.</strong><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2253"></span><span id="midl2253"></span><dl> <dt><strong>MIDL2253</strong></dt> </dl></td>
<td><dl> <dt><span id="array_types_with__transmit_as__or__represent_as__not_supported_on_return_type_for__Oi_modes___using__Os"></span><span id="array_types_with__transmit_as__or__represent_as__not_supported_on_return_type_for__oi_modes___using__os"></span><span id="ARRAY_TYPES_WITH__TRANSMIT_AS__OR__REPRESENT_AS__NOT_SUPPORTED_ON_RETURN_TYPE_FOR__OI_MODES___USING__OS"></span>Tipi di matrice con [transmit_as] o [represent_as] non supportati nel tipo restituito per le modalità /Oi , con /Os</dt> <dd> La restituzione di una matrice con [<a href="transmit-as.md"><strong>transmit_as</strong></a>] o [<a href="represent-as.md"><strong>represent_as</strong></a>] applicata può essere gestita solo dagli stub di ottimizzazione <a href="-os.md"><strong>/Os.</strong></a> Gli stub per questa routine verranno generati usando <strong>l'ottimizzazione /Os.</strong><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2254"></span><span id="midl2254"></span><dl> <dt><strong>MIDL2254</strong></dt> </dl></td>
<td><dl> <dt><span id="array_types_with__transmit_as__or__represent_as__not_supported_pass-by-value_for__Oi_modes__using__Os"></span><span id="array_types_with__transmit_as__or__represent_as__not_supported_pass-by-value_for__oi_modes__using__os"></span><span id="ARRAY_TYPES_WITH__TRANSMIT_AS__OR__REPRESENT_AS__NOT_SUPPORTED_PASS-BY-VALUE_FOR__OI_MODES__USING__OS"></span>Tipi di matrice con [transmit_as] o [represent_as] non supportati per le modalità /Oi, con /Os</dt> <dd> Questa azione non è supportata per l'ottimizzazione completamente interpretata. Passaggio all'ottimizzazione in modalità mista.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2255"></span><span id="midl2255"></span><dl> <dt><strong>MIDL2255</strong></dt> </dl></td>
<td><dl> <dt><span id="_callback__requires__ms_ext"></span><span id="_CALLBACK__REQUIRES__MS_EXT"></span>[callback] richiede /ms_ext</dt> <dd> <a href="callback.md"><strong>L'attributo</strong></a>[ callback ] è un'estensione Microsoft e richiede che l'opzione <a href="-ms-ext.md"><strong>/ms_ext</strong></a> sia abilitata. Non eseguire la compilazione con <a href="-osf.md"><strong>/osf</strong></a>, che esegue l'override <strong>di /ms_ext</strong>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2256"></span><span id="midl2256"></span><dl> <dt><strong>MIDL2256</strong></dt> </dl></td>
<td><dl> <dt><span id="circular_interface_dependency"></span><span id="CIRCULAR_INTERFACE_DEPENDENCY"></span>dipendenza dell'interfaccia circolare</dt> <dd> Questa interfaccia usa se stessa (direttamente o indirettamente) come interfaccia di base.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2257"></span><span id="midl2257"></span><dl> <dt><strong>MIDL2257</strong></dt> </dl></td>
<td><dl> <dt><span id="only_IUnknown_may_be_used_as_the_root_interface"></span><span id="only_iunknown_may_be_used_as_the_root_interface"></span><span id="ONLY_IUNKNOWN_MAY_BE_USED_AS_THE_ROOT_INTERFACE"></span>solo IUnknown può essere usato come interfaccia radice</dt> <dd> Attualmente, tutte le interfacce devono avere <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown"><strong>IUnknown</strong></a> come interfaccia radice.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2258"></span><span id="midl2258"></span><dl> <dt><strong>MIDL2258</strong></dt> </dl></td>
<td><dl> <dt><span id="_IID_IS__may_only_be_applied_to_pointers_to_interfaces"></span><span id="_iid_is__may_only_be_applied_to_pointers_to_interfaces"></span><span id="_IID_IS__MAY_ONLY_BE_APPLIED_TO_POINTERS_TO_INTERFACES"></span>[IID_IS] può essere applicato solo ai puntatori alle interfacce</dt> <dd> <a href="iid-is.md"><strong>L'attributo</strong></a>[ iid_is ] può essere applicato solo ai puntatori a interfaccia, anche se possono essere specificati come puntatori a <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown"><strong>IUnknown</strong></a> *.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2259"></span><span id="midl2259"></span><dl> <dt><strong>MIDL2259</strong></dt> </dl></td>
<td><dl> <dt><span id="interfaces_may_only_be_used_in_pointer-to-interface_constructs"></span><span id="INTERFACES_MAY_ONLY_BE_USED_IN_POINTER-TO-INTERFACE_CONSTRUCTS"></span>Le interfacce possono essere usate solo nei costrutti puntatore a interfaccia</dt> <dd> I nomi di interfaccia non possono essere usati se non come interfacce di base o puntatori a interfaccia.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2260"></span><span id="midl2260"></span><dl> <dt><strong>MIDL2260</strong></dt> </dl></td>
<td><dl> <dt><span id="interface_pointers_must_have_a_UUID_IID"></span><span id="interface_pointers_must_have_a_uuid_iid"></span><span id="INTERFACE_POINTERS_MUST_HAVE_A_UUID_IID"></span>I puntatori a interfaccia devono avere un UUID/IID</dt> <dd> Il tipo di base<a href="iid-is.md"><strong>dell'espressione</strong></a>[ iid_is ] deve essere un tipo UUID/GUID/IID.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2261"></span><span id="midl2261"></span><dl> <dt><strong>MIDL2261</strong></dt> </dl></td>
<td><dl> <dt><span id="definitions_and_declarations_outside_of_interface_body_requires__ms_ext"></span><span id="DEFINITIONS_AND_DECLARATIONS_OUTSIDE_OF_INTERFACE_BODY_REQUIRES__MS_EXT"></span>le definizioni e le dichiarazioni all'esterno del corpo dell'interfaccia richiedono /ms_ext</dt> <dd> L'inserimento di dichiarazioni e definizioni all'esterno di qualsiasi corpo dell'interfaccia è un'estensione Microsoft e richiede l'uso <a href="-ms-ext.md"><strong>dell'opzione /ms_ext.</strong></a><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2262"></span><span id="midl2262"></span><dl> <dt><strong>MIDL2262</strong></dt> </dl></td>
<td><dl> <dt><span id="multiple_interfaces_in_one_file_requires__ms_ext"></span><span id="MULTIPLE_INTERFACES_IN_ONE_FILE_REQUIRES__MS_EXT"></span>più interfacce in un file richiedono /ms_ext</dt> <dd> L'uso di più interfacce in un singolo file idl è un'estensione Microsoft e non è disponibile quando si esegue la compilazione in <a href="-osf.md"><strong>modalità /osf.</strong></a><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2263"></span><span id="midl2263"></span><dl> <dt><strong>MIDL2263</strong></dt> </dl></td>
<td><dl> <dt><span id="only_one_of__implicit_handle____auto_handle___or__explicit_handle__allowed"></span><span id="ONLY_ONE_OF__IMPLICIT_HANDLE____AUTO_HANDLE___OR__EXPLICIT_HANDLE__ALLOWED"></span>è consentito solo uno dei valori [implicit_handle], [auto_handle] o [explicit_handle]</dt> <dd> Ogni interfaccia può avere solo uno di questi tre attributi.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2264"></span><span id="midl2264"></span><dl> <dt><strong>MIDL2264</strong></dt> </dl></td>
<td><dl> <dt><span id="_implicit_handle__references_a_type_which_is_not_a_handle"></span><span id="_IMPLICIT_HANDLE__REFERENCES_A_TYPE_WHICH_IS_NOT_A_HANDLE"></span>[implicit_handle] fa riferimento a un tipo che non è un handle</dt> <dd> Gli handle impliciti devono essere di uno dei tipi di handle.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2265"></span><span id="midl2265"></span><dl> <dt><strong>MIDL2265</strong></dt> </dl></td>
<td><dl> <dt><span id="_object__procs_may_only_be_used_with___env_win32_"></span><span id="_OBJECT__PROCS_MAY_ONLY_BE_USED_WITH___ENV_WIN32_"></span>[object] procs può essere usato solo con &quot; /env win32&quot;</dt> <dd> Le interfacce con<a href="object.md"><strong>l'attributo</strong></a>[ object ] non possono essere usate con ambienti a 16 bit.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2266"></span><span id="midl2266"></span><dl> <dt><strong>MIDL2266</strong></dt> </dl></td>
<td><dl> <dt><span id="_callback__with_-env_dos_win16_not_supported_for__Oi__using__Os"></span><span id="_callback__with_-env_dos_win16_not_supported_for__oi__using__os"></span><span id="_CALLBACK__WITH_-ENV_DOS_WIN16_NOT_SUPPORTED_FOR__OI__USING__OS"></span>[callback] con -env dos/win16 non supportato per /Oi, con /Os</dt> <dd> I callback negli ambienti a 16 bit possono essere gestiti solo dagli stub <a href="-os.md"><strong>di ottimizzazione /Os.</strong></a> Gli stub per questa routine verranno generati usando <strong>l'ottimizzazione /Os.</strong><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2267"></span><span id="midl2267"></span><dl> <dt><strong>MIDL2267</strong></dt> </dl></td>
<td><dl> <dt><span id="float_double_not_supported_as_top-level_parameter_for__Oi_mode__using__Os"></span><span id="float_double_not_supported_as_top-level_parameter_for__oi_mode__using__os"></span><span id="FLOAT_DOUBLE_NOT_SUPPORTED_AS_TOP-LEVEL_PARAMETER_FOR__OI_MODE__USING__OS"></span>float/double non supportato come parametro di primo livello per la modalità /Oi, con /Os</dt> <dd> I tipi float e double possono essere gestiti solo come parametri dagli stub <a href="-os.md"><strong>di ottimizzazione /Os.</strong></a> Gli stub per questa routine verranno generati usando <strong>l'ottimizzazione /Os.</strong> I tipi float e double all'interno di strutture, matrici o unioni possono comunque essere gestiti con<strong>/Os</strong>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2268"></span><span id="midl2268"></span><dl> <dt><strong>MIDL2268</strong></dt> </dl></td>
<td><dl> <dt><span id="pointers_to_context_handles_may_not_be_used_as_return_values"></span><span id="POINTERS_TO_CONTEXT_HANDLES_MAY_NOT_BE_USED_AS_RETURN_VALUES"></span>I puntatori agli handle di contesto non possono essere usati come valori restituiti</dt> <dd> Gli handle di contesto devono essere usati come valori restituiti diretti, non come valori restituiti indiretti.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2269"></span><span id="midl2269"></span><dl> <dt><strong>MIDL2269</strong></dt> </dl></td>
<td><dl> <dt><span id="procedures_in_an_object_interface_must_return_an_HRESULT"></span><span id="procedures_in_an_object_interface_must_return_an_hresult"></span><span id="PROCEDURES_IN_AN_OBJECT_INTERFACE_MUST_RETURN_AN_HRESULT"></span>Le routine in un'interfaccia a oggetti devono restituire un HRESULT</dt> <dd> Tutte le routine in un'interfaccia a oggetti che non hanno l'attributo -[<a href="local.md"><strong>local</strong></a>] devono restituire <strong>un HRESULT</strong> / <strong>SCODE</strong>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2270"></span><span id="midl2270"></span><dl> <dt><strong>MIDL2270</strong></dt> </dl></td>
<td><dl> <dt><span id="duplicate_UUID"></span><span id="duplicate_uuid"></span><span id="DUPLICATE_UUID"></span>UUID duplicato</dt> <dd> Gli UUID devono essere univoci.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2271"></span><span id="midl2271"></span><dl> <dt><strong>MIDL2271</strong></dt> </dl></td>
<td><dl> <dt><span id="_object__interfaces_must_derive_from_another__object__interface_such_as_IUnknown"></span><span id="_object__interfaces_must_derive_from_another__object__interface_such_as_iunknown"></span><span id="_OBJECT__INTERFACES_MUST_DERIVE_FROM_ANOTHER__OBJECT__INTERFACE_SUCH_AS_IUNKNOWN"></span>Le interfacce [object] devono derivare da un'altra interfaccia [object], ad esempio IUnknown</dt> <dd> L'ereditarietà dell'interfaccia è consentita solo quando si usano le interfacce oggetto.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2272"></span><span id="midl2272"></span><dl> <dt><strong>MIDL2272</strong></dt> </dl></td>
<td><dl> <dt><span id="_async__interface_must_derive_from_another__async__interface"></span><span id="_ASYNC__INTERFACE_MUST_DERIVE_FROM_ANOTHER__ASYNC__INTERFACE"></span>L'interfaccia (asincrona) deve derivare da un'altra interfaccia (asincrona)</dt> <dd> Le interfacce oggetto, sincrone e asincrone, devono derivare da <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown"><strong>IUnknown</strong></a> o da un'altra interfaccia OLE di base.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2273"></span><span id="midl2273"></span><dl> <dt><strong>MIDL2273</strong></dt> </dl></td>
<td><dl> <dt><span id="_IID_IS__expression_must_be_a_pointer_to_IID_structure"></span><span id="_iid_is__expression_must_be_a_pointer_to_iid_structure"></span><span id="_IID_IS__EXPRESSION_MUST_BE_A_POINTER_TO_IID_STRUCTURE"></span>[IID_IS] l'espressione deve essere un puntatore alla struttura IID</dt> <dd> Il tipo di base<a href="iid-is.md"><strong>dell'espressione</strong></a>[ iid_is ] deve essere un tipo UUID/GUID/IID.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2274"></span><span id="midl2274"></span><dl> <dt><strong>MIDL2274</strong></dt> </dl></td>
<td><dl> <dt><span id="_call_as__type_must_be_a__local__procedure"></span><span id="_CALL_AS__TYPE_MUST_BE_A__LOCAL__PROCEDURE"></span>[call_as] il tipo deve essere una routine [local]</dt> <dd> Alla destinazione di un tipo [<a href="call-as.md"><strong>call_as</strong></a>] , se definito, deve essere applicato [ <a href="local.md"><strong>local</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2275"></span><span id="midl2275"></span><dl> <dt><strong>MIDL2275</strong></dt> </dl></td>
<td><dl> <dt><span id="undefined__call_as__must_not_be_used_in_an_object_interface"></span><span id="UNDEFINED__CALL_AS__MUST_NOT_BE_USED_IN_AN_OBJECT_INTERFACE"></span>undefined [call_as] non deve essere usato in un'interfaccia a oggetti</dt> <dd> È necessario definire la destinazione di un tipo [<a href="call-as.md"><strong>call_as</strong></a>]. Assicurarsi di aver fornito <strong>call_as</strong> routine per le applicazioni chiamanti e chiamate.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2276"></span><span id="midl2276"></span><dl> <dt><strong>MIDL2276</strong></dt> </dl></td>
<td><dl> <dt><span id="_auto_handle__may_not_be_used_with__encode__or__decode_"></span><span id="_AUTO_HANDLE__MAY_NOT_BE_USED_WITH__ENCODE__OR__DECODE_"></span>[auto_handle] non può essere usato con [encode] o [decode]</dt> <dd> Gli attributi [ <a href="encode.md"><strong>encode</strong></a>] e [ <a href="decode.md"><strong>decode</strong></a>] possono essere usati solo con handle espliciti o handle impliciti.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2277"></span><span id="midl2277"></span><dl> <dt><strong>MIDL2277</strong></dt> </dl></td>
<td><dl> <dt><span id="normal_procedures_are_not_allowed_in_an_interface_with__encode__or__decode_"></span><span id="NORMAL_PROCEDURES_ARE_NOT_ALLOWED_IN_AN_INTERFACE_WITH__ENCODE__OR__DECODE_"></span>Le procedure normali non sono consentite in un'interfaccia con [encode] o [decode]</dt> <dd> Anche le interfacce contenenti [<a href="encode.md"><strong>encode</strong></a>] o [<a href="decode.md"><strong>decode</strong></a>] non possono avere procedure remote.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2278"></span><span id="midl2278"></span><dl> <dt><strong>MIDL2278</strong></dt> </dl></td>
<td><dl> <dt><span id="top-level_conformance_or_variance_not_allowed_with__encode__or__decode_"></span><span id="TOP-LEVEL_CONFORMANCE_OR_VARIANCE_NOT_ALLOWED_WITH__ENCODE__OR__DECODE_"></span>conformità o varianza di primo livello non consentita con [encode] o [decode]</dt> <dd> I tipi con conformità o varianza di primo livello non possono usare la serializzazione dei tipi, poiché non è possibile fornire ridimensionamento/allungamento. Le strutture che le contengono possono tuttavia usare la serializzazione dei tipi.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2279"></span><span id="midl2279"></span><dl> <dt><strong>MIDL2279</strong></dt> </dl></td>
<td><dl> <dt><span id="_out__parameters_may_not_have__const_"></span><span id="_OUT__PARAMETERS_MAY_NOT_HAVE__CONST_"></span>I parametri [out] potrebbero non avere &quot; const&quot;</dt> <dd> Poiché un parametro [<a href="out-idl.md"><strong>out</strong></a>] viene modificato, non deve essere dichiarato come costante sa.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2280"></span><span id="midl2280"></span><dl> <dt><strong>MIDL2280</strong></dt> </dl></td>
<td><dl> <dt><span id="return_values_may_not_have__const_"></span><span id="RETURN_VALUES_MAY_NOT_HAVE__CONST_"></span>I valori restituiti non possono avere &quot; const&quot;</dt> <dd> Poiché un valore di funzione viene impostato quando la funzione viene restituita, questo valore non deve essere dichiarato come costante.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2281"></span><span id="midl2281"></span><dl> <dt><strong>MIDL2281</strong></dt> </dl></td>
<td><dl> <dt><span id="invalid_use_of__retval__attribute"></span><span id="INVALID_USE_OF__RETVAL__ATTRIBUTE"></span>Uso non valido &quot; dell'attributo &quot; retval</dt> <dd> Verificare di non aver usato l'attributo [<a href="optional.md"><strong>facoltativo</strong></a>] e che il parametro [<a href="retval.md"><strong>retval</strong></a>] sia l'ultimo parametro nell'elenco.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2282"></span><span id="midl2282"></span><dl> <dt><strong>MIDL2282</strong></dt> </dl></td>
<td><dl> <dt><span id="multiple_calling_conventions_illegal"></span><span id="MULTIPLE_CALLING_CONVENTIONS_ILLEGAL"></span>più convenzioni di chiamata non validi</dt> <dd> A una singola routine può essere applicata una sola convenzione di chiamata.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2283"></span><span id="midl2283"></span><dl> <dt><strong>MIDL2283</strong></dt> </dl></td>
<td><dl> <dt><span id="attribute_illegal_on__object__procedure"></span><span id="ATTRIBUTE_ILLEGAL_ON__OBJECT__PROCEDURE"></span>Attributo non valido nella routine [object]</dt> <dd> L'attributo precedente si applica solo alle procedure nelle interfacce che non hanno<a href="object.md"><strong>l'attributo</strong></a>[ object ].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2284"></span><span id="midl2284"></span><dl> <dt><strong>MIDL2284</strong></dt> </dl></td>
<td><dl> <dt><span id="_out__interface_pointers_must_use_double_indirection"></span><span id="_OUT__INTERFACE_POINTERS_MUST_USE_DOUBLE_INDIRECTION"></span>I puntatori a interfaccia [out] devono usare il riferimento indiretto doppio</dt> <dd> Poiché il valore modificato è il puntatore all'interfaccia, deve essere presente un altro livello di riferimento indiretto sopra il puntatore per consentirne la restituita.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2285"></span><span id="midl2285"></span><dl> <dt><strong>MIDL2285</strong></dt> </dl></td>
<td><dl> <dt><span id="procedure_used_twice_as_the_caller_in__call_as_"></span><span id="PROCEDURE_USED_TWICE_AS_THE_CALLER_IN__CALL_AS_"></span>Procedura usata due volte come chiamante in [call_as]</dt> <dd> Una determinata routine [<a href="local.md"><strong>local</strong></a>] può essere usata una sola volta come destinazione di un [<a href="call-as.md"><strong>call_as</strong></a>], per evitare conflitti tra nomi.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2286"></span><span id="midl2286"></span><dl> <dt><strong>MIDL2286</strong></dt> </dl></td>
<td><dl> <dt><span id="_call_as__target_must_have__local__in_an_object_interface"></span><span id="_CALL_AS__TARGET_MUST_HAVE__LOCAL__IN_AN_OBJECT_INTERFACE"></span>[call_as] la destinazione deve avere [local] in un'interfaccia a oggetti</dt> <dd> La destinazione di una [<a href="call-as.md"><strong>call_as</strong></a>] deve essere una routine [<a href="local.md"><strong>local</strong></a>] definita nell'interfaccia corrente.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2287"></span><span id="midl2287"></span><dl> <dt><strong>MIDL2287</strong></dt> </dl></td>
<td><dl> <dt><span id="_code__and__nocode__may_not_be_used_together"></span><span id="_CODE__AND__NOCODE__MAY_NOT_BE_USED_TOGETHER"></span>[code] e [nocode] non possono essere usati insieme</dt> <dd> Questi due attributi sono contraddittori e non possono essere usati insieme.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2288"></span><span id="midl2288"></span><dl> <dt><strong>MIDL2288</strong></dt> </dl></td>
<td><dl> <dt><span id="procedures_with__maybe__or__message__attributes_may_not_have__out__params__or_return_values_must_be_of_type_HRESULT_or_error_status_t"></span><span id="procedures_with__maybe__or__message__attributes_may_not_have__out__params__or_return_values_must_be_of_type_hresult_or_error_status_t"></span><span id="PROCEDURES_WITH__MAYBE__OR__MESSAGE__ATTRIBUTES_MAY_NOT_HAVE__OUT__PARAMS__OR_RETURN_VALUES_MUST_BE_OF_TYPE_HRESULT_OR_ERROR_STATUS_T"></span>Le routine con attributi [maybe] o [message] possono non avere parametri [out] o i valori restituiti devono essere di tipo HRESULT o error_status_t</dt> <dd> Poiché le procedure<a href="maybe.md"><strong>[ forse</strong></a>] non restituiscono mai, non è possibile ottenere valori restituiti.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2289"></span><span id="midl2289"></span><dl> <dt><strong>MIDL2289</strong></dt> </dl></td>
<td><dl> <dt><span id="pointer_to_function_must_be_used"></span><span id="POINTER_TO_FUNCTION_MUST_BE_USED"></span>È necessario usare il puntatore alla funzione</dt> <dd> Anche se le definizioni di tipo funzione sono consentite in <a href="-c-ext.md"><strong>modalità /c_ext,</strong></a> possono essere usate solo come puntatori a funzioni. Non possono mai essere trasmessi come parametro o come valore restituito di una procedura remota.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2290"></span><span id="midl2290"></span><dl> <dt><strong>MIDL2290</strong></dt> </dl></td>
<td><dl> <dt><span id="functions_may_not_be_passed_in_an_RPC_operation"></span><span id="functions_may_not_be_passed_in_an_rpc_operation"></span><span id="FUNCTIONS_MAY_NOT_BE_PASSED_IN_AN_RPC_OPERATION"></span>Le funzioni non possono essere passate in un'operazione RPC</dt> <dd> Le funzioni e i puntatori a funzione non possono essere passati come parametri o valori restituiti di procedure remote.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2291"></span><span id="midl2291"></span><dl> <dt><strong>MIDL2291</strong></dt> </dl></td>
<td><dl> <dt><span id="hyper_double_not_supported_as_return_value_for__Oi_modes__using__Os"></span><span id="hyper_double_not_supported_as_return_value_for__oi_modes__using__os"></span><span id="HYPER_DOUBLE_NOT_SUPPORTED_AS_RETURN_VALUE_FOR__OI_MODES__USING__OS"></span>hyper/double non supportato come valore restituito per le modalità /Oi, con /Os</dt> <dd> I valori restituiti Hyper e Double possono essere gestiti solo dagli stub <a href="-os.md"><strong>di ottimizzazione /Os.</strong></a> Gli stub per questa routine verranno generati usando <strong>l'ottimizzazione /Os.</strong><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2292"></span><span id="midl2292"></span><dl> <dt><strong>MIDL2292</strong></dt> </dl></td>
<td><dl> <dt><span id="_pragma_pack_pop__without_matching__pragma_pack_push_"></span><span id="_PRAGMA_PACK_POP__WITHOUT_MATCHING__PRAGMA_PACK_PUSH_"></span>#pragma pack(pop) senza corrispondenza #pragma pack(push)</dt> <dd> #pragma pack(push) e #pragma pack(pop) devono essere presenti in coppie corrispondenti. È stato specificato almeno un #pragma pack(push)s.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2293"></span><span id="midl2293"></span><dl> <dt><strong>MIDL2293</strong></dt> </dl></td>
<td><dl> <dt><span id="stringable_structure_fields_must_be_byte_char_wchar_t"></span><span id="STRINGABLE_STRUCTURE_FIELDS_MUST_BE_BYTE_CHAR_WCHAR_T"></span>I campi della struttura stringable devono essere byte/char/wchar_t</dt> <dd> Il tipo [<a href="string.md"><strong>string</strong></a>] può essere applicato solo a una struttura i cui campi sono tutti di tipo byte o a una definizione di tipo equivalente a byte.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2294"></span><span id="midl2294"></span><dl> <dt><strong>MIDL2294</strong></dt> </dl></td>
<td><dl> <dt><span id="_notify__not_supported_for__Oi_modes__using__Os"></span><span id="_notify__not_supported_for__oi_modes__using__os"></span><span id="_NOTIFY__NOT_SUPPORTED_FOR__OI_MODES__USING__OS"></span>[notify] non supportato per le modalità /Oi, con /Os</dt> <dd> <a href="notify.md"><strong>L'attributo</strong></a>[ notify ] può essere elaborato solo dagli stub <a href="-os.md"><strong>di ottimizzazione /Os.</strong></a><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2295"></span><span id="midl2295"></span><dl> <dt><strong>MIDL2295</strong></dt> </dl></td>
<td><dl> <dt><span id="_handle_parameter_or_return_type_is_not_supported_on_a_procedure_in_an__object__interface"></span><span id="_HANDLE_PARAMETER_OR_RETURN_TYPE_IS_NOT_SUPPORTED_ON_A_PROCEDURE_IN_AN__OBJECT__INTERFACE"></span> Il parametro handle o il tipo restituito non è supportato in una routine in un'interfaccia [object]</dt> <dd> Non è possibile usare handle con interfacce [ <a href="object.md"><strong>object</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2296"></span><span id="midl2296"></span><dl> <dt><strong>MIDL2296</strong></dt> </dl></td>
<td><dl> <dt><span id="ANSI_C_only_allows_the_leftmost_array_bound_to_be_unspecified"></span><span id="ansi_c_only_allows_the_leftmost_array_bound_to_be_unspecified"></span><span id="ANSI_C_ONLY_ALLOWS_THE_LEFTMOST_ARRAY_BOUND_TO_BE_UNSPECIFIED"></span>ANSI C consente solo che la matrice più a sinistra sia specificata</dt> <dd> In una matrice conforme ANSI C consente di non essere specificata solo la matrice più a sinistra (più significativa) associata. Se più dimensioni sono conformi, MIDL tenterà di inserire &quot; 1 &quot; nelle altre dimensioni conformi. Se le altre dimensioni sono definite in una definizione di tipo diversa, questa operazione non può essere possibile. Provare a inserire tutte le dimensioni della matrice nella dichiarazione di matrice per evitare questo problema. In ogni caso, fare attenzione ai calcoli di indicizzazione delle matrici ese nell'esecuzione del compilatore. potrebbe essere necessario eseguire calcoli personalizzati usando le dimensioni effettive.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2297"></span><span id="midl2297"></span><dl> <dt><strong>MIDL2297</strong></dt> </dl></td>
<td><dl> <dt><span id="by-value_union_parameters_not_supported_for__Oi_modes__using__Os"></span><span id="by-value_union_parameters_not_supported_for__oi_modes__using__os"></span><span id="BY-VALUE_UNION_PARAMETERS_NOT_SUPPORTED_FOR__OI_MODES__USING__OS"></span>Parametri di unione per valore non supportati per le modalità /Oi, con /Os</dt> <dd> Questa azione non è supportata per l'ottimizzazione completamente interpretata. Passaggio all'ottimizzazione in modalità mista.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2298"></span><span id="midl2298"></span><dl> <dt><strong>MIDL2298</strong></dt> </dl></td>
<td><dl> <dt><span id="_version__attribute_is_ignored_on_an__object__interface"></span><span id="_VERSION__ATTRIBUTE_IS_IGNORED_ON_AN__OBJECT__INTERFACE"></span>L'attributo [version] viene ignorato in un'interfaccia [object]</dt> <dd> <a href="object.md"><strong>L'attributo</strong></a>[ object ] identifica un'interfaccia COM. Un elenco di attributi di interfaccia per un'interfaccia COM non può includere <a href="version.md"><strong>l'attributo</strong></a>[ version ].<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2299"></span><span id="midl2299"></span><dl> <dt><strong>MIDL2299</strong></dt> </dl></td>
<td><dl> <dt><span id="_size_is__or__max_is__attribute_is_invalid_on_a_fixed_array"></span><span id="_SIZE_IS__OR__MAX_IS__ATTRIBUTE_IS_INVALID_ON_A_FIXED_ARRAY"></span>L'attributo [size_is] o [max_is] non è valido in una matrice fissa</dt> <dd> Le matrici di dimensioni fisse non possono usare gli <a href="size-is.md"><strong>size_is</strong></a> o <a href="max-is.md"><strong>max_is</strong></a> predefiniti.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2300"></span><span id="midl2300"></span><dl> <dt><strong>MIDL2300</strong></dt> </dl></td>
<td><dl> <dt><span id="_encode__or__decode__are_invalid_in_an__object__interface"></span><span id="_ENCODE__OR__DECODE__ARE_INVALID_IN_AN__OBJECT__INTERFACE"></span>[encode] o [decode] non sono validi in un'interfaccia [object]</dt> <dd> <a href="object.md"><strong>L'attributo</strong></a>[ object ] identifica un'interfaccia COM. Gli attributi [<a href="encode.md"><strong>encode</strong></a>] e [ <a href="decode.md"><strong>decode</strong></a>] abilitano la serializzazione. Ciò significa che è possibile fornire e controllare i buffer per il marshalling dei dati e l'unmarshal, ma non è possibile eseguire la serializzazione sulle interfacce COM.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2301"></span><span id="midl2301"></span><dl> <dt><strong>MIDL2301</strong></dt> </dl></td>
<td><dl> <dt><span id="_encode__or__decode__on_a_type_requires__ms_ext"></span><span id="_ENCODE__OR__DECODE__ON_A_TYPE_REQUIRES__MS_EXT"></span>[encode] o [decode] in un tipo richiede /ms_ext</dt> <dd> La serializzazione non fa parte della specifica DCE-IDL. Si tratta di un'estensione Microsoft che richiede l'uso <a href="-ms-ext.md"><strong>dell'opzione della riga di ms_ext /ms_ext.</strong></a><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2302"></span><span id="midl2302"></span><dl> <dt><strong>MIDL2302</strong></dt> </dl></td>
<td><dl> <dt><span id="int_not_supported_on__env_win16_or__env_dos"></span><span id="INT_NOT_SUPPORTED_ON__ENV_WIN16_OR__ENV_DOS"></span>int non supportato in /env win16 o /env dos</dt> <dd> Le piattaforme Microsoft a 16 bit non supportano l'uso del tipo <a href="int.md"><strong>int</strong></a> in un file IDL. Qualificare <strong>il tipo int</strong> con <a href="small.md"><strong>small</strong></a>, <a href="short.md"><strong>short</strong></a>o <a href="long.md"><strong>long.</strong></a><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2303"></span><span id="midl2303"></span><dl> <dt><strong>MIDL2303</strong></dt> </dl></td>
<td><dl> <dt><span id="_bstring__may_only_be_applied_to_a_pointer_to__char__or__whchar_t_"></span><span id="_BSTRING__MAY_ONLY_BE_APPLIED_TO_A_POINTER_TO__CHAR__OR__WHCHAR_T_"></span>[bstring] può essere applicato solo a un puntatore a &quot; char &quot; o &quot; whchar_t&quot;</dt> <dd> Questo errore è obsoleto. Viene fornito solo per compatibilità con le versioni precedenti.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2304"></span><span id="midl2304"></span><dl> <dt><strong>MIDL2304</strong></dt> </dl></td>
<td><dl> <dt><span id="attribute_invalid_on_a_procedure_in_an__object__interface"></span><span id="ATTRIBUTE_INVALID_ON_A_PROCEDURE_IN_AN__OBJECT__INTERFACE"></span>Attributo non valido in una routine in un'interfaccia [object]</dt> <dd> L'attributo specificato non è consentito nella procedura in un'interfaccia COM.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2305"></span><span id="midl2305"></span><dl> <dt><strong>MIDL2305</strong></dt> </dl></td>
<td><dl> <dt><span id="attribute_invalid_on_an__object__interface"></span><span id="ATTRIBUTE_INVALID_ON_AN__OBJECT__INTERFACE"></span>Attributo non valido in un'interfaccia [object]</dt> <dd> L'attributo specificato non è consentito in un'interfaccia COM.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2306"></span><span id="midl2306"></span><dl> <dt><strong>MIDL2306</strong></dt> </dl></td>
<td><dl> <dt><span id="too_many_parameters_or_stack_too_big_for__Oi_modes__using__Os"></span><span id="too_many_parameters_or_stack_too_big_for__oi_modes__using__os"></span><span id="TOO_MANY_PARAMETERS_OR_STACK_TOO_BIG_FOR__OI_MODES__USING__OS"></span>troppi parametri o stack troppo grandi per le modalità /Oi, con /Os</dt> <dd> Questo avviso è obsoleto. Viene fornito solo per compatibilità con le versioni precedenti. Indica che la chiamata alla procedura remota fa aumentare le dimensioni dello stack di oltre 64 K.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2307"></span><span id="midl2307"></span><dl> <dt><strong>MIDL2307</strong></dt> </dl></td>
<td><dl> <dt><span id="no_attributes_on_ACF_file_typedef__so_no_effect"></span><span id="no_attributes_on_acf_file_typedef__so_no_effect"></span><span id="NO_ATTRIBUTES_ON_ACF_FILE_TYPEDEF__SO_NO_EFFECT"></span>nessun attributo nel typedef del file ACF, quindi nessun effetto</dt> <dd> Il file IDL deve contenere tutte le istruzioni typedef che non dispongono di attributi. Non devono essere presenti nei file ACF. In caso contrario, il compilatore MIDL li interpreta come ridondanti e li ignora.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2308"></span><span id="midl2308"></span><dl> <dt><strong>MIDL2308</strong></dt> </dl></td>
<td><dl> <dt><span id="calling_conventions_other_than___stdcall_or___cdecl_not_supported_for__Oi_modes__using__Os"></span><span id="calling_conventions_other_than___stdcall_or___cdecl_not_supported_for__oi_modes__using__os"></span><span id="CALLING_CONVENTIONS_OTHER_THAN___STDCALL_OR___CDECL_NOT_SUPPORTED_FOR__OI_MODES__USING__OS"></span>Convenzioni di chiamata diverse __stdcall o __cdecl non sono supportate per le modalità /Oi, con /Os</dt> <dd> Le convenzioni di chiamata <strong>__pascal</strong> o <strong>__fastcall</strong> modificano il formato dello stack. Le <a href="-oi.md"><strong>modalità /Oi</strong></a> supportano solo <strong>le</strong> __stdcall e <strong>__cdecl</strong> di chiamata. Se è necessario utilizzare altre convenzioni di chiamata, utilizzare <a href="-os.md"><strong>la modalità /Os.</strong></a><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2309"></span><span id="midl2309"></span><dl> <dt><strong>MIDL2309</strong></dt> </dl></td>
<td><dl> <dt><span id="Too_many_delegation_methods_in_the_interface__require_Windows_2000_or_greater"></span><span id="too_many_delegation_methods_in_the_interface__require_windows_2000_or_greater"></span><span id="TOO_MANY_DELEGATION_METHODS_IN_THE_INTERFACE__REQUIRE_WINDOWS_2000_OR_GREATER"></span>Troppi metodi di delega nell'interfaccia, che richiedono Windows 2000 o versione successiva</dt> <dd> Un'interfaccia può ereditare da un'altra. In questo caso, i metodi dell'interfaccia di base vengono considerati delegati. Nessuna interfaccia derivata può contenere più di 256 metodi delegati.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2310"></span><span id="midl2310"></span><dl> <dt><strong>MIDL2310</strong></dt> </dl></td>
<td><dl> <dt><span id="auto_handles_not_supported_with__env_mac_or__env_powermac"></span><span id="AUTO_HANDLES_NOT_SUPPORTED_WITH__ENV_MAC_OR__ENV_POWERMAC"></span>Handle automatici non supportati con /env mac o /env powermac</dt> <dd> Quando si compila il file IDL per PowerMac, non è possibile usare handle di associazione automatici. È necessario specificare handle espliciti o impliciti.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2311"></span><span id="midl2311"></span><dl> <dt><strong>MIDL2311</strong></dt> </dl></td>
<td><dl> <dt><span id="statements_outside_library_block_are_illegal_in_mktyplib_compatibility_mode"></span><span id="STATEMENTS_OUTSIDE_LIBRARY_BLOCK_ARE_ILLEGAL_IN_MKTYPLIB_COMPATIBILITY_MODE"></span>Le istruzioni all'esterno del blocco di libreria non sono validi in modalità di compatibilità mktyplib</dt> <dd> Potrebbe essere necessario specificare l'opzione della riga di comando <a href="-mktyplib203.md"><strong>/mktyplib203</strong></a> quando si compila il file IDL.<br/>
<blockquote>
[!Note]<br />
Lo Mktyplib.exe è obsoleto. In alternativa, usare il compilatore MIDL.
</blockquote>
<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2312"></span><span id="midl2312"></span><dl> <dt><strong>MIDL2312</strong></dt> </dl></td>
<td><dl> <dt><span id="illegal_syntax_unless_using_mktyplib_compatibility_mode"></span><span id="ILLEGAL_SYNTAX_UNLESS_USING_MKTYPLIB_COMPATIBILITY_MODE"></span>sintassi non valida a meno che non si utilizzi la modalità di compatibilità mktyplib</dt> <dd> Potrebbe essere necessario specificare l'opzione della riga di comando <a href="-mktyplib203.md"><strong>/mktyplib203</strong></a> quando si compila il file IDL.<br/>
<blockquote>
[!Note]<br />
Lo Mktyplib.exe è obsoleto. In alternativa, usare il compilatore MIDL.
</blockquote>
<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2313"></span><span id="midl2313"></span><dl> <dt><strong>MIDL2313</strong></dt> </dl></td>
<td><dl> <dt><span id="illegal_definition__must_use_typedef_in_mktyplib_compatibility_mode"></span><span id="ILLEGAL_DEFINITION__MUST_USE_TYPEDEF_IN_MKTYPLIB_COMPATIBILITY_MODE"></span>definizione non valida, deve usare typedef in modalità di compatibilità mktyplib</dt> <dd> Potrebbe essere necessario specificare l'opzione della riga di comando <a href="-mktyplib203.md"><strong>/mktyplib203</strong></a> quando si compila il file IDL.<br/>
<blockquote>
[!Note]<br />
Lo Mktyplib.exe è obsoleto. In alternativa, usare il compilatore MIDL.
</blockquote>
<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2314"></span><span id="midl2314"></span><dl> <dt><strong>MIDL2314</strong></dt> </dl></td>
<td><dl> <dt><span id="explicit_pointer_attribute__ptr___ref__ignored_for_interface_pointers"></span><span id="EXPLICIT_POINTER_ATTRIBUTE__PTR___REF__IGNORED_FOR_INTERFACE_POINTERS"></span>attributo puntatore esplicito [ptr] [ref] ignorato per i puntatori a interfaccia</dt> <dd> I puntatori alle interfacce non possono avere attributi IDL.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2315"></span><span id="midl2315"></span><dl> <dt><strong>MIDL2315</strong></dt> </dl></td>
<td><a href="-oi.md"><strong>Modalità /Oi</strong></a> non implementate per PowerMac, passaggio a <a href="-os.md"> <strong>/Os</strong></a><br/></td>
</tr>
<tr class="odd">
<td><span id="MIDL2316"></span><span id="midl2316"></span><dl> <dt><strong>MIDL2316</strong></dt> </dl></td>
<td><dl> <dt><span id="illegal_expression_type_used_in_attribute"></span><span id="ILLEGAL_EXPRESSION_TYPE_USED_IN_ATTRIBUTE"></span>tipo di espressione non valido usato nell'attributo</dt> <dd> Il valore predefinito per il puntatore deve essere una costante.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2317"></span><span id="midl2317"></span><dl> <dt><strong>MIDL2317</strong></dt> </dl></td>
<td><dl> <dt><span id="illegal_type_used_in_pipe"></span><span id="ILLEGAL_TYPE_USED_IN_PIPE"></span>tipo non valido usato nella pipe</dt> <dd> Le pipe sono limitate ai tipi di dati IDL di base. Ad esempio, non è possibile specificare una pipe di matrici.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2318"></span><span id="midl2318"></span><dl> <dt><strong>MIDL2318</strong></dt> </dl></td>
<td><dl> <dt><span id="procedure_uses_pipes__using__Oicf"></span><span id="procedure_uses_pipes__using__oicf"></span><span id="PROCEDURE_USES_PIPES__USING__OICF"></span>la stored procedure usa le pipe, con /Oicf</dt> <dd> La modalità selezionata non supporta le pipe. Il compilatore MIDL ha rilevato l'uso di una o più pipe nell'interfaccia. Pertanto, compila il file IDL in <a href="-oi.md"><strong>modalità /Oicf.</strong></a><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2319"></span><span id="midl2319"></span><dl> <dt><strong>MIDL2319</strong></dt> </dl></td>
<td><dl> <dt><span id="procedure_has_an_attribute_that_requires_use_of__Oif__switching_modes"></span><span id="procedure_has_an_attribute_that_requires_use_of__oif__switching_modes"></span><span id="PROCEDURE_HAS_AN_ATTRIBUTE_THAT_REQUIRES_USE_OF__OIF__SWITCHING_MODES"></span>la routine ha un attributo che richiede l'uso di /Oif, modalità di cambio</dt> <dd> È necessario compilare le procedure [<a href="async.md"><strong>async</strong></a>] in <a href="-oi.md"><strong>modalità /Oif.</strong></a><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2320"></span><span id="midl2320"></span><dl> <dt><strong>MIDL2320</strong></dt> </dl></td>
<td><dl> <dt><span id="conflicting_optimization_requirements__cannot_optimize"></span><span id="CONFLICTING_OPTIMIZATION_REQUIREMENTS__CANNOT_OPTIMIZE"></span>requisiti di ottimizzazione in conflitto, non è possibile ottimizzare</dt> <dd> Questo errore indica spesso che sono stati specificati sia <a href="-os.md"><strong>/Os</strong></a> che <a href="-oi.md"><strong>/Oi</strong></a> (o una variante delle modalità del compilatore <strong>MIDL /Oi</strong>). Può anche significare che le funzionalità specificate nei file IDL e ACL richiedono l'uso di entrambe le modalità. È necessario selezionare una modalità o l'altra per l'ottimizzazione.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2321"></span><span id="midl2321"></span><dl> <dt><strong>MIDL2321</strong></dt> </dl></td>
<td><dl> <dt><span id="pipes_cannot_be_array_elements__or_members_of_structures_or_unions"></span><span id="PIPES_CANNOT_BE_ARRAY_ELEMENTS__OR_MEMBERS_OF_STRUCTURES_OR_UNIONS"></span>Le pipe non possono essere elementi di matrice o membri di strutture o unioni</dt> <dd> I tipi di dati della pipe possono essere solo parametri di primo livello.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2322"></span><span id="midl2322"></span><dl> <dt><strong>MIDL2322</strong></dt> </dl></td>
<td><dl> <dt><span id="invalid_pipe_usage"></span><span id="INVALID_PIPE_USAGE"></span>utilizzo della pipe non valido</dt> <dd> Non è possibile usare pipe con gli attributi [<a href="transmit-as.md"><strong>transmit_as</strong></a>], [<a href="represent-as.md"><strong>represent_as</strong></a>] o [<a href="user-marshal.md"><strong>user_marshal</strong></a>]. Inoltre, le pipe non possono essere usate come tipi restituiti.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2323"></span><span id="midl2323"></span><dl> <dt><strong>MIDL2323</strong></dt> </dl></td>
<td><dl> <dt><span id="feature_requires_the_advanced_interpreted_optimization_option__use_-Oicf"></span><span id="feature_requires_the_advanced_interpreted_optimization_option__use_-oicf"></span><span id="FEATURE_REQUIRES_THE_ADVANCED_INTERPRETED_OPTIMIZATION_OPTION__USE_-OICF"></span>la funzionalità richiede l'opzione di ottimizzazione interpretata avanzata. usare -Oicf</dt> <dd> Questo errore indica che le opzioni della riga di comando del compilatore MIDL, ad esempio <a href="-robust.md"><strong>/robust,</strong></a> richiedono l'uso della <a href="-oi.md"><strong>modalità /Oicf.</strong></a><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2324"></span><span id="midl2324"></span><dl> <dt><strong>MIDL2324</strong></dt> </dl></td>
<td><dl> <dt><span id="feature_requires_the_advanced_interpreted_optimization_option__use_-Oicf"></span><span id="feature_requires_the_advanced_interpreted_optimization_option__use_-oicf"></span><span id="FEATURE_REQUIRES_THE_ADVANCED_INTERPRETED_OPTIMIZATION_OPTION__USE_-OICF"></span>la funzionalità richiede l'opzione di ottimizzazione interpretata avanzata. usare -Oicf</dt> <dd> Questo avviso indica che le opzioni della riga di comando del compilatore MIDL, ad esempio <a href="-robust.md"><strong>/robust,</strong></a> richiedono l'uso della <a href="-oi.md"><strong>modalità /Oicf.</strong></a><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2329"></span><span id="midl2329"></span><dl> <dt><strong>MIDL2329</strong></dt> </dl></td>
<td><dl> <dt><span id="the_optimization_option_is_being_phased_out__use_-Oic"></span><span id="the_optimization_option_is_being_phased_out__use_-oic"></span><span id="THE_OPTIMIZATION_OPTION_IS_BEING_PHASED_OUT__USE_-OIC"></span>l'opzione di ottimizzazione è in fase di implementazione. Usare -Oic</dt> <dd> La <a href="-oi.md"><strong>modalità di ottimizzazione /Oi1</strong></a> è stata specificata nella riga di comando MIDL. Questa modalità non è più supportata ed <strong>è necessario usare /Oicf.</strong><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2330"></span><span id="midl2330"></span><dl> <dt><strong>MIDL2330</strong></dt> </dl></td>
<td><dl> <dt><span id="the_optimization_option_is_being_phased_out__use_-Oicf"></span><span id="the_optimization_option_is_being_phased_out__use_-oicf"></span><span id="THE_OPTIMIZATION_OPTION_IS_BEING_PHASED_OUT__USE_-OICF"></span>l'opzione di ottimizzazione è in fase di implementazione. Usare -Oicf</dt> <dd> La <a href="-oi.md"><strong>modalità di ottimizzazione /Oi2</strong></a> è stata specificata nella riga di comando MIDL. Questa modalità non è più supportata ed <strong>è necessario usare /Oicf.</strong><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2331"></span><span id="midl2331"></span><dl> <dt><strong>MIDL2331</strong></dt> </dl></td>
<td><dl> <dt><span id="the_optimization_option_is_being_phased_out__use_-ic"></span><span id="THE_OPTIMIZATION_OPTION_IS_BEING_PHASED_OUT__USE_-IC"></span>l'opzione di ottimizzazione è in fase di uscita. Usare -ic</dt> <dd> La modalità di ottimizzazione i1 è stata specificata in un attributo ACF [optimize]. Questa modalità non è più supportata ed è necessario usare invece icf.<br/> File ACF di esempio:<br/>
<pre class="syntax" data-space="preserve"><code>[optimize(&quot;i1&quot;)] roo();    //MIDL 2331</code></pre>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2332"></span><span id="midl2332"></span><dl> <dt><strong>MIDL2332</strong></dt> </dl></td>
<td><dl> <dt><span id="the_optimization_option_is_being_phased_out__use_-icf"></span><span id="THE_OPTIMIZATION_OPTION_IS_BEING_PHASED_OUT__USE_-ICF"></span>l'opzione di ottimizzazione è in fase di uscita. Usare -icf</dt> <dd> La modalità di ottimizzazione i2 è stata specificata in un attributo ACF [optimize]. Questa modalità non è più supportata ed è necessario usare invece icf.<br/> File ACF di esempio:<br/>
<pre class="syntax" data-space="preserve"><code>[optimize(&quot;i2&quot;)] roo();    //MIDL 2332</code></pre>
</dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2333"></span><span id="midl2333"></span><dl> <dt><strong>MIDL2333</strong></dt> </dl></td>
<td><dl> <dt><span id="the_-old_and_-new_switches_are_obsolete__use_-oldtlb_and_-newtlb"></span><span id="THE_-OLD_AND_-NEW_SWITCHES_ARE_OBSOLETE__USE_-OLDTLB_AND_-NEWTLB"></span>Le opzioni -old e -new sono obsolete. Usare -oldtlb e -newtlb</dt> <dd> Questo messaggio è obsoleto e non viene più omesso da MIDL.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2334"></span><span id="midl2334"></span><dl> <dt><strong>MIDL2334</strong></dt> </dl></td>
<td><dl> <dt><span id="illegal_argument_value"></span><span id="ILLEGAL_ARGUMENT_VALUE"></span>valore di argomento non valido</dt> <dd> Le varianti consentite dell'opzione della riga di comando /O includono <a href="-os.md"><strong>/Os</strong></a>, <a href="-oi.md"><strong>/Oi</strong></a>, <strong>/Oic</strong>, <strong>/Oicf</strong>e <strong>/Oif</strong>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2335"></span><span id="midl2335"></span><dl> <dt><strong>MIDL2335</strong></dt> </dl></td>
<td><dl> <dt><span id="illegal_expression_type_in_constant"></span><span id="ILLEGAL_EXPRESSION_TYPE_IN_CONSTANT"></span>tipo di espressione non valido nella costante</dt> <dd> L'espressione non restituisce una costante.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2336"></span><span id="midl2336"></span><dl> <dt><strong>MIDL2336</strong></dt> </dl></td>
<td><dl> <dt><span id="illegal_expression_type_in_enum"></span><span id="ILLEGAL_EXPRESSION_TYPE_IN_ENUM"></span>tipo di espressione non valido nell'enumerazione</dt> <dd> Un valore enumerato in una <a href="enum.md"><strong>definizione di enumerazione</strong></a> non restituisce un tipo integrale.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2337"></span><span id="midl2337"></span><dl> <dt><strong>MIDL2337</strong></dt> </dl></td>
<td><dl> <dt><span id="unsatisfied_forward_declaration"></span><span id="UNSATISFIED_FORWARD_DECLARATION"></span>dichiarazione con inoltro non soddisfatta</dt> <dd> Il compilatore MIDL non è stato in grado di risolvere la definizione di una dichiarazione con inoltro.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2338"></span><span id="midl2338"></span><dl> <dt><strong>MIDL2338</strong></dt> </dl></td>
<td><dl> <dt><span id="switches_are_contradictory"></span><span id="SWITCHES_ARE_CONTRADICTORY"></span>Opzioni contraddittorie</dt> <dd> Non è possibile usare entrambe le opzioni della riga di comando <a href="-osf.md"><strong>/osf</strong></a> e <a href="-ms-ext.md"><strong>/ms_ext</strong></a> quando si compila un file IDL. È necessario scegliere uno o l'altro.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2339"></span><span id="midl2339"></span><dl> <dt><strong>MIDL2339</strong></dt> </dl></td>
<td><dl> <dt><span id="MIDL_cannot_generate_HOOKOLE_information_for_the_non-rpc-able_union"></span><span id="midl_cannot_generate_hookole_information_for_the_non-rpc-able_union"></span><span id="MIDL_CANNOT_GENERATE_HOOKOLE_INFORMATION_FOR_THE_NON-RPC-ABLE_UNION"></span>MIDL non può generare informazioni HOOKOLE per l'unione non rpc-able</dt> <dd> Questo errore è obsoleto. Viene fornito esclusivamente per garantire la compatibilità con le versioni precedenti.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2340"></span><span id="midl2340"></span><dl> <dt><strong>MIDL2340</strong></dt> </dl></td>
<td><dl> <dt><span id="no_case_expression_found_for_union"></span><span id="NO_CASE_EXPRESSION_FOUND_FOR_UNION"></span>nessuna espressione case trovata per union</dt> <dd> Ogni campo di un'unione deve avere un'istruzione case con un'espressione costante.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2341"></span><span id="midl2341"></span><dl> <dt><strong>MIDL2341</strong></dt> </dl></td>
<td><dl> <dt><span id="_user_marshal__and__wire_marshal__not_supported_with_-Oi_and_-Oic_flags__use_-Os_or_-Oicf"></span><span id="_user_marshal__and__wire_marshal__not_supported_with_-oi_and_-oic_flags__use_-os_or_-oicf"></span><span id="_USER_MARSHAL__AND__WIRE_MARSHAL__NOT_SUPPORTED_WITH_-OI_AND_-OIC_FLAGS__USE_-OS_OR_-OICF"></span>[user_marshal] e [wire_marshal] non supportati con i flag -Oi e -Oic, usare -Os o -Oicf</dt> <dd> Gli attributi [<a href="user-marshal.md"><strong>user_marshal</strong></a>] e [<a href="wire-marshal.md"><strong>wire_marshal</strong></a>] richiedono le funzionalità di ottimizzazione specifiche disponibili solo in <a href="-oi.md"><strong>/Oicf</strong></a> (proxy senza codice con stringhe di formato rapido) o <a href="-os.md"><strong>/Os</strong></a> (marshalling in modalità mista).<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2342"></span><span id="midl2342"></span><dl> <dt><strong>MIDL2342</strong></dt> </dl></td>
<td><dl> <dt><span id="pipes_can_t_be_used_with_data_serialization__i.e.__encode__and_or__decode_"></span><span id="PIPES_CAN_T_BE_USED_WITH_DATA_SERIALIZATION__I.E.__ENCODE__AND_OR__DECODE_"></span>Le pipe non possono essere usate con la serializzazione dei dati, ad esempio [encode] e/o [decode]</dt> <dd> Non è possibile passare le pipe come parametri alle routine con gli attributi [<a href="encode.md"><strong>encode</strong></a>] o [<a href="decode.md"><strong>decode</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2343"></span><span id="midl2343"></span><dl> <dt><strong>MIDL2343</strong></dt> </dl></td>
<td><dl> <dt><span id="all_pipe_interface_pointers_must_use_single_indirection"></span><span id="ALL_PIPE_INTERFACE_POINTERS_MUST_USE_SINGLE_INDIRECTION"></span>tutti i puntatori di interfaccia della pipe devono usare un riferimento indiretto singolo</dt> <dd> Non è possibile usare un puntatore a un puntatore a un'interfaccia pipe in questo modo.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2344"></span><span id="midl2344"></span><dl> <dt><strong>MIDL2344</strong></dt> </dl></td>
<td><dl> <dt><span id="_iid_is____cannot_be_used_with_a_pipe_interface_pointer"></span><span id="_IID_IS____CANNOT_BE_USED_WITH_A_PIPE_INTERFACE_POINTER"></span>[iid_is()] non può essere usato con un puntatore di interfaccia pipe</dt> <dd> Questo messaggio è obsoleto. Questo messaggio non viene più usato dal compilatore.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2345"></span><span id="midl2345"></span><dl> <dt><strong>MIDL2345</strong></dt> </dl></td>
<td><dl> <dt><span id="invalid_or_inapplicable_-lcid_switch"></span><span id="INVALID_OR_INAPPLICABLE_-LCID_SWITCH"></span>opzione -lcid non valida o non valida</dt> <dd> L'identificatore locale (LCID) specificato non è valido.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2346"></span><span id="midl2346"></span><dl> <dt><strong>MIDL2346</strong></dt> </dl></td>
<td><dl> <dt><span id="the_specified_lcid_is_different_from_previous_specification"></span><span id="THE_SPECIFIED_LCID_IS_DIFFERENT_FROM_PREVIOUS_SPECIFICATION"></span>l'lcid specificato è diverso dalla specifica precedente</dt> <dd> I valori specificati in /lcid e [<a href="lcid.md"><strong>lcid</strong></a>] sono diversi. Il compilatore MIDL userà l'ultimo definito.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2347"></span><span id="midl2347"></span><dl> <dt><strong>MIDL2347</strong></dt> </dl></td>
<td><dl> <dt><span id="importlib_is_not_allowed_outside_of_a_library_block"></span><span id="IMPORTLIB_IS_NOT_ALLOWED_OUTSIDE_OF_A_LIBRARY_BLOCK"></span>importlib non è consentito all'esterno di un blocco di libreria</dt> <dd> Tutte le istruzioni [<a href="importlib.md"><strong>importlib</strong></a>] devono essere eseguite in un blocco [<a href="library.md"><strong>library</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2348"></span><span id="midl2348"></span><dl> <dt><strong>MIDL2348</strong></dt> </dl></td>
<td><dl> <dt><span id="invalid_floating_point_value"></span><span id="INVALID_FLOATING_POINT_VALUE"></span>Valore a virgola mobile non valido</dt> <dd> Questo errore non deve essere generato da MIDL. Se viene visualizzato questo errore, segnalare un bug a Microsoft fornendo tutti i file necessari per riprodurre l'errore, inclusi i file IDL, i file ACF, le intestazioni e così via.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2349"></span><span id="midl2349"></span><dl> <dt><strong>MIDL2349</strong></dt> </dl></td>
<td><dl> <dt><span id="invalid_member"></span><span id="INVALID_MEMBER"></span>membro non valido</dt> <dd> Le procedure non possono essere membri di una libreria.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2350"></span><span id="midl2350"></span><dl> <dt><strong>MIDL2350</strong></dt> </dl></td>
<td><dl> <dt><span id="possible_invalid_member"></span><span id="POSSIBLE_INVALID_MEMBER"></span>possibile membro non valido</dt> <dd> Per essere un membro valido di una libreria, l'elemento della libreria deve essere un modulo, un'interfaccia dispatch, una coclasse, un'istruzione if, una struttura, un'unione, un'enumerazione o una dichiarazione con inoltro.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2351"></span><span id="midl2351"></span><dl> <dt><strong>MIDL2351</strong></dt> </dl></td>
<td><dl> <dt><span id="mismatch_in_pipe_and_interface_types"></span><span id="MISMATCH_IN_PIPE_AND_INTERFACE_TYPES"></span>mancata corrispondenza nei tipi pipe e di interfaccia</dt> <dd> Questo messaggio è obsoleto.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2352"></span><span id="midl2352"></span><dl> <dt><strong>MIDL2352</strong></dt> </dl></td>
<td><dl> <dt><span id="string__varying_array__conformant_array_and_full_pointer_parameters_may_be_incompatible_with_pipe_parameters_during_run_time"></span><span id="STRING__VARYING_ARRAY__CONFORMANT_ARRAY_AND_FULL_POINTER_PARAMETERS_MAY_BE_INCOMPATIBLE_WITH_PIPE_PARAMETERS_DURING_RUN_TIME"></span>string, varying array, conformant array and full pointer parameters may be incompatible with pipe parameters during run time</dt> <dd> Un metodo che combina una o più stringhe [in], matrici variabili, matrici conformi e parametri di puntatore completi e qualsiasi parametro [in] pipe genera uno stub che viene eseguito solo in sequenze di protocollo <strong>ncacn_*</strong> e <a href="ncalrpc.md"><strong>ncalrpc</strong></a> nei computer Windows. L'uso dello stub per effettuare chiamate su sequenze di protocollo <strong>ncadg_*</strong> o accettare chiamate da altri fornitori RPC DCE OSF può generare errori nel server durante la fase di esecuzione. Questo errore si verifica a partire da Windows Server 2003.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2353"></span><span id="midl2353"></span><dl> <dt><strong>MIDL2353</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_must_be_in"></span><span id="PARAMETER_MUST_BE_IN"></span>il parametro deve essere in</dt> <dd> Gli handle asincroni devono essere parametri [<a href="in.md"><strong>in</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2354"></span><span id="midl2354"></span><dl> <dt><strong>MIDL2354</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_type_of_an__async__object_must_be_a_double_pointer_to_an_interface"></span><span id="PARAMETER_TYPE_OF_AN__ASYNC__OBJECT_MUST_BE_A_DOUBLE_POINTER_TO_AN_INTERFACE"></span>il tipo di parametro di un oggetto [async] deve essere un puntatore double a un'interfaccia</dt> <dd> Il parametro deve essere di tipo <strong>IAsyncManager</strong> **.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2355"></span><span id="midl2355"></span><dl> <dt><strong>MIDL2355</strong></dt> </dl></td>
<td><dl> <dt><span id="incorrect_async_handle_type"></span><span id="INCORRECT_ASYNC_HANDLE_TYPE"></span>tipo di handle asincrono non corretto</dt> <dd> Il tipo di handle deve <strong>essere IAsyncManager</strong> o un tipo derivato da <strong>IAsyncManager</strong>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2356"></span><span id="midl2356"></span><dl> <dt><strong>MIDL2356</strong></dt> </dl></td>
<td><dl> <dt><span id="the__internal__switch_enables_unsupported_features__use_with_caution"></span><span id="THE__INTERNAL__SWITCH_ENABLES_UNSUPPORTED_FEATURES__USE_WITH_CAUTION"></span>il &quot; &quot; commutatore interno abilita le funzionalità non supportate, usare con cautela</dt> <dd> Evitare di usare questa opzione.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2357"></span><span id="midl2357"></span><dl> <dt><strong>MIDL2357</strong></dt> </dl></td>
<td><dl> <dt><span id="async_procedures_cannot_use_auto_handle"></span><span id="ASYNC_PROCEDURES_CANNOT_USE_AUTO_HANDLE"></span>Le procedure asincrone non possono usare la gestione automatica</dt> <dd> Le routine con l'attributo [<a href="async.md"><strong>async</strong></a>] richiedono handle espliciti.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2358"></span><span id="midl2358"></span><dl> <dt><strong>MIDL2358</strong></dt> </dl></td>
<td><dl> <dt><span id="error_status_t_should_have_both__comm_status__and__fault_status_"></span><span id="ERROR_STATUS_T_SHOULD_HAVE_BOTH__COMM_STATUS__AND__FAULT_STATUS_"></span>error_status_t deve avere sia [comm_status] che [fault_status]</dt> <dd> È stata specificata una routine con gli attributi IDL [forse] o [message] ma il tipo restituito ha solo gli attributi ACF [comm_status] o [fault_status]. Entrambi gli attributi ACF sono obbligatori.<br/> File ACF di esempio:<br/>
<pre class="syntax" data-space="preserve"><code>[comm_status] roo();    //MIDL 2358
[fault_status] bar();    //MIDL 2358
[comm_status, fault_status] baz();    //OK</code></pre>
</dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2359"></span><span id="midl2359"></span><dl> <dt><strong>MIDL2359</strong></dt> </dl></td>
<td><dl> <dt><span id="this_construct_is_only_allowed_within_a_library_block"></span><span id="THIS_CONSTRUCT_IS_ONLY_ALLOWED_WITHIN_A_LIBRARY_BLOCK"></span>Questo costrutto è consentito solo all'interno di un blocco di libreria</dt> <dd> Un modulo può verificarsi solo all'interno di un blocco di libreria.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2360"></span><span id="midl2360"></span><dl> <dt><strong>MIDL2360</strong></dt> </dl></td>
<td><dl> <dt><span id="invalid_type_redefinition"></span><span id="INVALID_TYPE_REDEFINITION"></span>ridefinizione del tipo non valida</dt> <dd> Un nuovo tipo è stato definito in modo ricorsivo in un tipo non esistente.<br/> Esempio:<br/>
<pre class="syntax" data-space="preserve"><code>typedef roo roo[10];    //MIDL 2360</code></pre>
</dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2361"></span><span id="midl2361"></span><dl> <dt><strong>MIDL2361</strong></dt> </dl></td>
<td><dl> <dt><span id="procedures_with_a__vararg__attribute_must_have_a_SAFEARRAY_VARIANT__parameter__param_order_is__vararg____lcid____retval_"></span><span id="procedures_with_a__vararg__attribute_must_have_a_safearray_variant__parameter__param_order_is__vararg____lcid____retval_"></span><span id="PROCEDURES_WITH_A__VARARG__ATTRIBUTE_MUST_HAVE_A_SAFEARRAY_VARIANT__PARAMETER__PARAM_ORDER_IS__VARARG____LCID____RETVAL_"></span>Le routine con un attributo [vararg] devono avere un parametro SAFEARRAY(VARIANT). param order è [vararg], [lcid], [retval]</dt> <dd> La maggior parte dei parametri per le routine con l'attributo [<a href="vararg.md"><strong>vararg</strong></a>] deve essere eseguita prima del <strong>parametro SAFEARRAY(VARIANT).</strong> Il <strong>parametro SAFEARRAY(VARIANT)</strong> deve essere presente. Se l'elenco di parametri contiene un parametro con l'attributo [ <a href="lcid.md"><strong>lcid</strong></a>], deve seguire il <strong>parametro SAFEARRAY(VARIANT).</strong> Se l'elenco di parametri contiene un parametro con l'attributo [<a href="retval.md"><strong>retval</strong></a>], deve verificarsi dopo il parametro con l'attributo [<strong>lcid</strong>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2363"></span><span id="midl2363"></span><dl> <dt><strong>MIDL2363</strong></dt> </dl></td>
<td><dl> <dt><span id="too_many_methods_in_the_interface__requires_Windows_2000_or_greater"></span><span id="too_many_methods_in_the_interface__requires_windows_2000_or_greater"></span><span id="TOO_MANY_METHODS_IN_THE_INTERFACE__REQUIRES_WINDOWS_2000_OR_GREATER"></span>troppi metodi nell'interfaccia, richiede Windows 2000 o versione successiva</dt> <dd> Il compilatore MIDL non consente più di 1024 metodi in un'interfaccia durante la compilazione in <a href="-oi.md"><strong>modalità /Oicf.</strong></a><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2364"></span><span id="midl2364"></span><dl> <dt><strong>MIDL2364</strong></dt> </dl></td>
<td><dl> <dt><span id="switch_is_being_phased_out"></span><span id="SWITCH_IS_BEING_PHASED_OUT"></span>È in corso l'uscita graduale dell'opzione</dt> <dd> Le opzioni seguenti sono obsolete: /<strong>hookole</strong>, /<strong>env win16</strong>e<strong>/env</strong>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2365"></span><span id="midl2365"></span><dl> <dt><strong>MIDL2365</strong></dt> </dl></td>
<td><dl> <dt><span id="cannot_derive_from_IAdviseSink__IAdviseSink2__or_IAdviseSinkEx"></span><span id="cannot_derive_from_iadvisesink__iadvisesink2__or_iadvisesinkex"></span><span id="CANNOT_DERIVE_FROM_IADVISESINK__IADVISESINK2__OR_IADVISESINKEX"></span>non può derivare da IAdviseSink, IAdviseSink2 o IAdviseSinkEx</dt> <dd> Queste interfacce non possono essere estese.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2366"></span><span id="midl2366"></span><dl> <dt><strong>MIDL2366</strong></dt> </dl></td>
<td><dl> <dt><span id="cannot_assign_a_default_value"></span><span id="CANNOT_ASSIGN_A_DEFAULT_VALUE"></span>impossibile assegnare un valore predefinito</dt> <dd> L'assegnazione di un valore predefinito a un parametro è consentita Visual Basic, ma non in C++. Se si usa C++, il valore predefinito viene ignorato.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2367"></span><span id="midl2367"></span><dl> <dt><strong>MIDL2367</strong></dt> </dl></td>
<td><dl> <dt><span id="type_library_generation_for_DOS_Win16_MAC_is_not_supported"></span><span id="type_library_generation_for_dos_win16_mac_is_not_supported"></span><span id="TYPE_LIBRARY_GENERATION_FOR_DOS_WIN16_MAC_IS_NOT_SUPPORTED"></span>La generazione della libreria dei tipi per DOS/Win16/MAC non è supportata</dt> <dd> MIDL non supporta librerie dei tipi a 16 bit.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2368"></span><span id="midl2368"></span><dl> <dt><strong>MIDL2368</strong></dt> </dl></td>
<td><dl> <dt><span id="error_generating_type_library__ignored"></span><span id="ERROR_GENERATING_TYPE_LIBRARY__IGNORED"></span>errore durante la generazione della libreria dei tipi, ignorato</dt> <dd> Si è verificato un errore non irreversibile durante la generazione della libreria dei tipi.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2369"></span><span id="midl2369"></span><dl> <dt><strong>MIDL2369</strong></dt> </dl></td>
<td><dl> <dt><span id="exceeded_stack_size_for__Oi__using__Os"></span><span id="exceeded_stack_size_for__oi__using__os"></span><span id="EXCEEDED_STACK_SIZE_FOR__OI__USING__OS"></span>superata la dimensione dello stack per /Oi, con /Os</dt> <dd> La modalità di ottimizzazione -Oi è limitata a 128 byte di spazio dello stack per i parametri. Il compilatore è passata automaticamente alla modalità di ottimizzazione del sistema operativo per aggirare questa limitazione.<br/> Per evitare questo avviso, usare le modalità di ottimizzazione -Oicf o -Os. La modalità di ottimizzazione può essere modificata nella riga di comando specificando -Oicf o -Os anziché -Oi oppure aggiungendo un attributo [optimize9 &quot; icf )] o optimize[( s )] alla funzione nel &quot; &quot; file &quot; ACF.<br/> Questo avviso si verifica in genere quando si passano strutture di grandi dimensioni come parametri per valore. Le dimensioni dello stack richieste possono essere ridotte passando invece un puntatore alla struttura .<br/> Esempio:<br/>
<pre class="syntax" data-space="preserve"><code>typedef struct
{
char a[127];
}
large;
//This function has a stack size of 132 (x86) or 136 (alpha) on 32-bit systems
void roo(large s, int a);    //MIDL 2360
// workaround: pass by reference
void bar (large *s, int a);</code></pre>
</dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2370"></span><span id="midl2370"></span><dl> <dt><strong>MIDL2370</strong></dt> </dl></td>
<td><dl> <dt><span id="use_of__robust_requires__Oicf__switching_modes"></span><span id="use_of__robust_requires__oicf__switching_modes"></span><span id="USE_OF__ROBUST_REQUIRES__OICF__SWITCHING_MODES"></span>l'uso di /robust richiede /Oicf, modalità di cambio</dt> <dd> È necessario eseguire la compilazione in <a href="-oi.md"><strong>modalità /Oicf</strong></a> quando si specifica l'opzione <a href="-robust.md"><strong>/robust</strong></a> nella riga di comando.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2371"></span><span id="midl2371"></span><dl> <dt><strong>MIDL2371</strong></dt> </dl></td>
<td><dl> <dt><span id="incorrect_range_specified"></span><span id="INCORRECT_RANGE_SPECIFIED"></span>intervallo non corretto specificato</dt> <dd> Il valore più alto specificato in un attributo [<a href="range.md"><strong>range</strong></a>] è minore del valore più basso.<br/> Esempio:<br/>
<pre class="syntax" data-space="preserve"><code>void roo([range(3,2)] int a);    //MIDL 2371</code></pre>
</dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2372"></span><span id="midl2372"></span><dl> <dt><strong>MIDL2372</strong></dt> </dl></td>
<td><dl> <dt><span id="_invalid_combination_of__in__only_and__out__parameters_for__async_uuid__interface"></span><span id="_INVALID_COMBINATION_OF__IN__ONLY_AND__OUT__PARAMETERS_FOR__ASYNC_UUID__INTERFACE"></span> Combinazione non valida dei parametri [in] e [out] per l'interfaccia [async_uuid]</dt> <dd> Per questo tipo di interfaccia sono consentite solo semplici combinazioni di attributi con parametri [<a href="in.md"><strong>in</strong></a>] o [<a href="out-idl.md"><strong>out</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2373"></span><span id="midl2373"></span><dl> <dt><strong>MIDL2373</strong></dt> </dl></td>
<td><dl> <dt><span id="DOS__Win16_and_MAC_platforms_are_not_supported_with__robust"></span><span id="dos__win16_and_mac_platforms_are_not_supported_with__robust"></span><span id="DOS__WIN16_AND_MAC_PLATFORMS_ARE_NOT_SUPPORTED_WITH__ROBUST"></span>Le piattaforme DOS, Win16 e MAC non sono supportate con /robust</dt> <dd> MIDL supporta <a href="-robust.md"><strong>l'opzione /robust</strong></a> in Microsoft Windows 2000 o versione successiva.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2374"></span><span id="midl2374"></span><dl> <dt><strong>MIDL2374</strong></dt> </dl></td>
<td><dl> <dt><span id="support_for_NT_3.51_style_stubless_proxies_for_object_interfaces_will_be_phased_out__use__Oif."></span><span id="support_for_nt_3.51_style_stubless_proxies_for_object_interfaces_will_be_phased_out__use__oif."></span><span id="SUPPORT_FOR_NT_3.51_STYLE_STUBLESS_PROXIES_FOR_OBJECT_INTERFACES_WILL_BE_PHASED_OUT__USE__OIF."></span>il supporto per i proxy stubless in stile NT 3.51 per le interfacce oggetto verrà gradualmente arrestato; usare /Oif.</dt> <dd> Questa modalità è obsoleta. Usare <a href="-oi.md"><strong>/Oif</strong></a> o <strong>/Oicf</strong>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2375"></span><span id="midl2375"></span><dl> <dt><strong>MIDL2375</strong></dt> </dl></td>
<td><dl> <dt><span id="_encode__or__decode__with__robust_requires__Oicf"></span><span id="_encode__or__decode__with__robust_requires__oicf"></span><span id="_ENCODE__OR__DECODE__WITH__ROBUST_REQUIRES__OICF"></span>[encode] o [decode] con /robust richiede /Oicf</dt> <dd> Non è possibile eseguire la serializzazione quando viene specificata <a href="-robust.md"><strong>l'opzione /robust.</strong></a><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2377"></span><span id="midl2377"></span><dl> <dt><strong>MIDL2377</strong></dt> </dl></td>
<td><dl> <dt><span id="conflicting_attributes_specified"></span><span id="CONFLICTING_ATTRIBUTES_SPECIFIED"></span>attributi in conflitto specificati</dt> <dd> Sono stati<a href="context-handle-serialize.md"><strong>specificati sia [ context_handle_serialize</strong></a>] che [<a href="context-handle-noserialize.md"><strong>context_handle_noserialize</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2378"></span><span id="midl2378"></span><dl> <dt><strong>MIDL2378</strong></dt> </dl></td>
<td><dl> <dt><span id="_serialize____noserialize__can_be_applied_to_context_handles"></span><span id="_SERIALIZE____NOSERIALIZE__CAN_BE_APPLIED_TO_CONTEXT_HANDLES"></span>[serialize], [noserialize] può essere applicato a context_handles</dt> <dd> Gli attributi ACF [context_handle_serialize] o [context_handle_noserialize] possono essere applicati solo ai tipi che sono handle di contesto.<br/> File IDL di esempio:<br/>
<pre class="syntax" data-space="preserve"><code>typedef /*[context_handle] */ void *PV;    //Note: PV is *not* a context handle.</code></pre>
File ACF di esempio:<br/>
<pre class="syntax" data-space="preserve"><code>typedef [context_handle_serialize] PV;    //MIDL 2378</code></pre>
</dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2379"></span><span id="midl2379"></span><dl> <dt><strong>MIDL2379</strong></dt> </dl></td>
<td><dl> <dt><span id="The_compiler_reached_a_limit_for_a_format_string_representation._See_documentation_for_advice."></span><span id="the_compiler_reached_a_limit_for_a_format_string_representation._see_documentation_for_advice."></span><span id="THE_COMPILER_REACHED_A_LIMIT_FOR_A_FORMAT_STRING_REPRESENTATION._SEE_DOCUMENTATION_FOR_ADVICE."></span>Il compilatore ha raggiunto un limite per una rappresentazione di stringa di formato. Per consigli, vedere la documentazione.</dt> <dd> Il compilatore MIDL ha un limite di 64 KB per le stringhe di formato. Questo errore si verifica in genere quando i file IDL includono altri file IDL. Il file IDL composito generato da tutte le istruzioni include supera i limiti delle tabelle di rappresentazione dei tipi dell'interprete del motore di marshalling. Provare a usare la direttiva import anziché la direttiva include nei file IDL. Per altre informazioni, vedere <a href="importing-system-header-files.md">Importazione di file di intestazione di sistema</a>, <a href="include.md"><strong>includere</strong></a>e <a href="import.md"><strong>importare</strong></a>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2380"></span><span id="midl2380"></span><dl> <dt><strong>MIDL2380</strong></dt> </dl></td>
<td><dl> <dt><span id="wire_format_may_be_incorrect__you_may_need_to_use_-ms_conf_struct__see_documentation_for_advice"></span><span id="WIRE_FORMAT_MAY_BE_INCORRECT__YOU_MAY_NEED_TO_USE_-MS_CONF_STRUCT__SEE_DOCUMENTATION_FOR_ADVICE"></span>il formato wire potrebbe non essere corretto, potrebbe essere necessario usare -ms_conf_struct, vedere la documentazione per consigli</dt> <dd> Il compilatore MIDL non è stato in grado di generare un formato trasmissibile per i dati. Un modo comune per ottenere questo errore è definire un ms_conf_struct <strong>all'interno</strong> di una struttura complessa.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2381"></span><span id="midl2381"></span><dl> <dt><strong>MIDL2381</strong></dt> </dl></td>
<td><dl> <dt><span id="a_stack_size_or_an_offset_bigger_than_64_K_limit._See_documentation_for_advice."></span><span id="a_stack_size_or_an_offset_bigger_than_64_k_limit._see_documentation_for_advice."></span><span id="A_STACK_SIZE_OR_AN_OFFSET_BIGGER_THAN_64_K_LIMIT._SEE_DOCUMENTATION_FOR_ADVICE."></span>una dimensione dello stack o un offset maggiore del limite di 64 K. Per consigli, vedere la documentazione.</dt> <dd> La chiamata comporta uno stack maggiore di 64 KB. Provare a passare i dati in blocchi più piccoli.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2382"></span><span id="midl2382"></span><dl> <dt><strong>MIDL2382</strong></dt> </dl></td>
<td><dl> <dt><span id="an_interpreter_mode_forced_for_64-bit_platform_"></span><span id="AN_INTERPRETER_MODE_FORCED_FOR_64-BIT_PLATFORM_"></span>modalità interprete forzata per la piattaforma a 64 bit </dt> <dd> Le piattaforme a 64 bit richiedono la modalità di compilazione /Oicf.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2383"></span><span id="midl2383"></span><dl> <dt><strong>MIDL2383</strong></dt> </dl></td>
<td><dl> <dt><span id="The_array_element_size_is_bigger_than_64_KB_limit."></span><span id="the_array_element_size_is_bigger_than_64_kb_limit."></span><span id="THE_ARRAY_ELEMENT_SIZE_IS_BIGGER_THAN_64_KB_LIMIT."></span>La dimensione dell'elemento della matrice è maggiore del limite di 64 KB.</dt> <dd> Tutte le dimensioni di tutti gli elementi della matrice devono essere inferiori a 64 KB.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2384"></span><span id="midl2384"></span><dl> <dt><strong>MIDL2384</strong></dt> </dl></td>
<td><dl> <dt><span id="there_can_be_only_one__Icid__parameter_in_a_method__and_it_should_be_last_or_second_to_last_if_last_parameter_has__retval_"></span><span id="there_can_be_only_one__icid__parameter_in_a_method__and_it_should_be_last_or_second_to_last_if_last_parameter_has__retval_"></span><span id="THERE_CAN_BE_ONLY_ONE__ICID__PARAMETER_IN_A_METHOD__AND_IT_SHOULD_BE_LAST_OR_SECOND_TO_LAST_IF_LAST_PARAMETER_HAS__RETVAL_"></span>può essere presente un solo parametro [Icid] in un metodo e deve essere ultimo o secondo all'ultimo se l'ultimo parametro ha [retval]</dt> <dd> Un parametro con l'attributo [<a href="lcid.md"><strong>lcid</strong></a>] deve verificarsi per ultimo. L'unica eccezione si verifica quando è presente anche un parametro con l'attributo [<a href="retval.md"><strong>retval</strong></a>]. Quando si verificano entrambi, il secondo all'ultimo parametro nell'elenco di parametri deve avere l'attributo [ <strong>lcid</strong>]. L'ultimo parametro deve avere l'attributo [<strong>retval</strong>].<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2385"></span><span id="midl2385"></span><dl> <dt><strong>MIDL2385</strong></dt> </dl></td>
<td><dl> <dt><span id="incorrect_syntax_for_midl_pragma"></span><span id="INCORRECT_SYNTAX_FOR_MIDL_PRAGMA"></span>Sintassi non corretta per midl_pragma</dt> <dd> Il compilatore MIDL ha rilevato un errore di sintassi sconosciuto in un midl_pragma istruzione .<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2386"></span><span id="midl2386"></span><dl> <dt><strong>MIDL2386</strong></dt> </dl></td>
<td><dl> <dt><span id="__int3264_is_not_supported_in__osf_mode"></span><span id="__INT3264_IS_NOT_SUPPORTED_IN__OSF_MODE"></span>__int3264 non è supportato in modalità /osf</dt> <dd> Se è necessario usare __int3264, compilare in modalità /ms-ext.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2387"></span><span id="midl2387"></span><dl> <dt><strong>MIDL2387</strong></dt> </dl></td>
<td><dl> <dt><span id="unresolved_symbol_in_type_library"></span><span id="UNRESOLVED_SYMBOL_IN_TYPE_LIBRARY"></span>simbolo non risolto nella libreria dei tipi</dt> <dd> Il compilatore non è stato in grado di risolvere una dichiarazione formale o un tipo a cui si fa riferimento nella libreria dei tipi.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2388"></span><span id="midl2388"></span><dl> <dt><strong>MIDL2388</strong></dt> </dl></td>
<td><dl> <dt><span id="async_pipes_cannot_be_passed_by_value"></span><span id="ASYNC_PIPES_CANNOT_BE_PASSED_BY_VALUE"></span>Le pipe asincrone non possono essere passate per valore</dt> <dd> Le pipe asincrone devono essere passate per riferimento o per indirizzo.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2389"></span><span id="midl2389"></span><dl> <dt><strong>MIDL2389</strong></dt> </dl></td>
<td><dl> <dt><span id="parameter_offset_exceed_64-KB_limit_for_interpreted_procedures"></span><span id="parameter_offset_exceed_64-kb_limit_for_interpreted_procedures"></span><span id="PARAMETER_OFFSET_EXCEED_64-KB_LIMIT_FOR_INTERPRETED_PROCEDURES"></span>l'offset del parametro supera il limite di 64 KB per le procedure interpretate</dt> <dd> Questo errore indica in genere che una routine ha troppi parametri.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2390"></span><span id="midl2390"></span><dl> <dt><strong>MIDL2390</strong></dt> </dl></td>
<td><dl> <dt><span id="invalid_array_element"></span><span id="INVALID_ARRAY_ELEMENT"></span>elemento di matrice non valido</dt> <dd> Le pipe non possono essere usate come elementi di matrice.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2391"></span><span id="midl2391"></span><dl> <dt><strong>MIDL2391</strong></dt> </dl></td>
<td><dl> <dt><span id="dispinterface_members_must_be_methods__properties_or_interfaces"></span><span id="DISPINTERFACE_MEMBERS_MUST_BE_METHODS__PROPERTIES_OR_INTERFACES"></span>I membri dell'interfaccia dispatch devono essere metodi, proprietà o interfacce</dt> <dd> Un'interfaccia dispatch non può contenere definizioni di tipo, strutture, enumerazioni o unioni.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2392"></span><span id="midl2392"></span><dl> <dt><strong>MIDL2392</strong></dt> </dl></td>
<td><dl> <dt><span id="_local__procedure_without__call_as_"></span><span id="_LOCAL__PROCEDURE_WITHOUT__CALL_AS_"></span>Routine [local] senza [call_as]</dt> <dd> Le routine oggetto con<a href="local.md"><strong>l'attributo</strong></a>[ local ] richiedono anche l'attributo [<a href="call-as.md"><strong>call_as</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2393"></span><span id="midl2393"></span><dl> <dt><strong>MIDL2393</strong></dt> </dl></td>
<td><dl> <dt><span id="multi_dimensional_vector__switching_to__Oicf"></span><span id="multi_dimensional_vector__switching_to__oicf"></span><span id="MULTI_DIMENSIONAL_VECTOR__SWITCHING_TO__OICF"></span>vettore multidimensionale, passaggio a /Oicf</dt> <dd> La <a href="-os.md"><strong>modalità di ottimizzazione /Os</strong></a> non supporta matrici di dimensioni non multidimensionali. Il compilatore ha automaticamente commutato la modalità di ottimizzazione su<strong>/Oicf</strong> per questa funzione. <br/> Questo avviso può essere eliminato a livello globale modificando la modalità del compilatore specificando<strong>/Oicf</strong> nella riga di comando MIDL o usando un avviso <strong>midl_pragma</strong> (disabilitazione: 2393) nel file IDL. La modalità di ottimizzazione può essere modificata per una singola funzione aggiungendo l'attributo [<strong>optimize( &quot; icf &quot; )</strong>] alla funzione nel file ACF.<br/> L'esempio seguente illustra questo avviso:<br/>
<pre class="syntax" data-space="preserve"><code>void roo(long s1, [size_is(s1)] long a[][30];    //MIDL2393
void bar(long s1, long s2, [size_is(s1,s2) long **a);//MIDL2393</code></pre>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2395"></span><span id="midl2395"></span><dl> <dt><strong>MIDL2395</strong></dt> </dl></td>
<td><dl> <dt><span id="type_or_construct_not_supported_in_a_library_block_because_Oleaut32.dll_support_for_64-KB_polymorphic_types_is_missing"></span><span id="type_or_construct_not_supported_in_a_library_block_because_oleaut32.dll_support_for_64-kb_polymorphic_types_is_missing"></span><span id="TYPE_OR_CONSTRUCT_NOT_SUPPORTED_IN_A_LIBRARY_BLOCK_BECAUSE_OLEAUT32.DLL_SUPPORT_FOR_64-KB_POLYMORPHIC_TYPES_IS_MISSING"></span>tipo o costrutto non supportato in un blocco di libreria perché manca Oleaut32.dll supporto per i tipi polimorfici da 64 KB</dt> <dd> L'automazione OLE non supporta tipi polimorfici ,ad esempio _int3264, INT_PTR e così via. Questi tipi hanno rappresentazioni di dati incompatibili tra piattaforme a 32 bit e a 64 bit. La chiamata remota avrà esito negativo in fase di esecuzione su piattaforme a 64 bit.<br/>
<blockquote>
[!Note]<br />
Si noti che Windows versione 2000, i file TLB a 64 bit sono supportati dall'automazione OLE convertendo le informazioni TLB a 32 bit in fase di esecuzione. Pertanto, solo la generazione di TLB a 32 bit è supportata da MIDL.
</blockquote>
<br/> Se MIDL viene usato solo per generare un file di intestazione, l'opzione <a href="-notlb.md"><strong>/notlb</strong></a> elimina la generazione del file TLB.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2396"></span><span id="midl2396"></span><dl> <dt><strong>MIDL2396</strong></dt> </dl></td>
<td><dl> <dt><span id="old_interpreter_code_being_generated_for_64b"></span><span id="OLD_INTERPRETER_CODE_BEING_GENERATED_FOR_64B"></span>codice dell'interprete precedente generato per 64b</dt> <dd> Questo errore è obsoleto. Se viene visualizzato questo errore, segnalare un bug a Microsoft fornendo i file IDL, i file ACF e la riga di comando MIDL completa.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2397"></span><span id="midl2397"></span><dl> <dt><strong>MIDL2397</strong></dt> </dl></td>
<td><dl> <dt><span id="the_compiler_switch_is_not_supported_anymore"></span><span id="THE_COMPILER_SWITCH_IS_NOT_SUPPORTED_ANYMORE"></span>L'opzione del compilatore non è più supportata</dt> <dd> L'opzione o le opzioni specificate non sono più supportate.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2398"></span><span id="midl2398"></span><dl> <dt><strong>MIDL2398</strong></dt> </dl></td>
<td><dl> <dt><span id="cannot_execute_MIDL_engine"></span><span id="cannot_execute_midl_engine"></span><span id="CANNOT_EXECUTE_MIDL_ENGINE"></span>impossibile eseguire il motore MIDL</dt> <dd> A data della versione Windows 2000 (MIDL versione 5.03.279), il compilatore MIDL viene implementato usando due file eseguibili: Midl.exe (driver) e Midlc.exe (motore del compilatore). Questo errore indica che il Midl.exe non è in grado di avviare Midlc.exe. Assicurarsi che Midlc.exe si trova nella stessa directory Midl.exe e che siano della stessa versione.<br/> L'errore potrebbe essere stato causato dalla copia Midl.exe ma non Midlx.exe dalla distribuzione più recente. Eseguire <strong>midl</strong> e/o <strong>midlc</strong> dalla riga di comando senza parametri per visualizzare il numero di versione del file eseguibile.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2399"></span><span id="midl2399"></span><dl> <dt><strong>MIDL2399</strong></dt> </dl></td>
<td><dl> <dt><span id="bad_commands_from_driver"></span><span id="BAD_COMMANDS_FROM_DRIVER"></span>Comandi non supportati dal driver</dt> <dd> A data della versione Windows 2000 (MIDL versione 5.03.279), il compilatore MIDL viene implementato usando due file eseguibili: Midl.exe (driver) e Midlc.exe (motore del compilatore). Questo errore indica che il file temporaneo usato per passare i comandi da Midl.exe a Midlc.exe è mancante o danneggiato. Assicurarsi che Midlc.exe si trova nella stessa directory Midl.exe e che siano della stessa versione.<br/> L'errore potrebbe essere stato causato dal tentativo di eseguire Midlc.exe direttamente o copiando Midl.exe ma non Midlc.exe dalla distribuzione più recente. Eseguire <strong>midl</strong> e/o <strong>midlc</strong> dalla riga di comando senza parametri per visualizzare il numero di versione del file eseguibile.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2400"></span><span id="midl2400"></span><dl> <dt><strong>MIDL2400</strong></dt> </dl></td>
<td><dl> <dt><span id="for_ole_automation__optional_parameters_should_be_VARIANT_or_VARIANT__"></span><span id="for_ole_automation__optional_parameters_should_be_variant_or_variant__"></span><span id="FOR_OLE_AUTOMATION__OPTIONAL_PARAMETERS_SHOULD_BE_VARIANT_OR_VARIANT__"></span>per l'automazione ole, i parametri facoltativi devono essere VARIANT o VARIANT *</dt> <dd> L'automazione OLE richiede che tutti i parametri [facoltativi] siano di tipo <strong>VARIANT</strong> o <strong>VARIANT*.</strong><br/> Nell'automazione OLE l'uso di parametri non VARIANT può causare l'esito negativo della chiamata in fase di esecuzione o il passaggio di dati non definiti per i parametri [<a href="optional.md"><strong>facoltativi</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2401"></span><span id="midl2401"></span><dl> <dt><strong>MIDL2401</strong></dt> </dl></td>
<td><dl> <dt><span id="_defaultvalue__is_applied_to_a_non-VARIANT_and__optional_._Please_remove__optional_"></span><span id="_defaultvalue__is_applied_to_a_non-variant_and__optional_._please_remove__optional_"></span><span id="_DEFAULTVALUE__IS_APPLIED_TO_A_NON-VARIANT_AND__OPTIONAL_._PLEASE_REMOVE__OPTIONAL_"></span>[defaultvalue] viene applicato a un tipo non VARIANT e [facoltativo]. Rimuovere [facoltativo]</dt> <dd> L'attributo [<a href="defaultvalue.md"><strong>defaultvalue</strong></a>] implica [<a href="optional.md"><strong>facoltativo</strong></a>]. L'attributo [ <strong>facoltativo</strong>] non è necessario.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2402"></span><span id="midl2402"></span><dl> <dt><strong>MIDL2402</strong></dt> </dl></td>
<td><dl> <dt><span id="_optional__attribute_is_inapplicable_outside_of_a_library_block"></span><span id="_OPTIONAL__ATTRIBUTE_IS_INAPPLICABLE_OUTSIDE_OF_A_LIBRARY_BLOCK"></span>Attributo [facoltativo] non valido all'esterno di un blocco di libreria</dt> <dd> La funzionalità implicita dell'attributo [ <a href="optional.md"><strong>facoltativo</strong></a>] non è applicabile ai proxy generati per un'interfaccia all'esterno di un blocco di libreria.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2403"></span><span id="midl2403"></span><dl> <dt><strong>MIDL2403</strong></dt> </dl></td>
<td><dl> <dt><span id="The_data_type_of_the__Icid__parameter_must_be_long"></span><span id="the_data_type_of_the__icid__parameter_must_be_long"></span><span id="THE_DATA_TYPE_OF_THE__ICID__PARAMETER_MUST_BE_LONG"></span>Il tipo di dati del parametro [Icid] deve essere long</dt> <dd> L'automazione OLE richiede che i parametri con<strong>l'attributo [ Icid</strong>] siano di tipo <a href="long.md"><strong>long.</strong></a><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2404"></span><span id="midl2404"></span><dl> <dt><strong>MIDL2404</strong></dt> </dl></td>
<td><dl> <dt><span id="procedures_with__propput____propget__or__propref__can_t_have_more_than_one_required_parameter_after__optional__one"></span><span id="PROCEDURES_WITH__PROPPUT____PROPGET__OR__PROPREF__CAN_T_HAVE_MORE_THAN_ONE_REQUIRED_PARAMETER_AFTER__OPTIONAL__ONE"></span>Le routine con [propput], [propget] o [propref] non possono avere più di un parametro obbligatorio dopo uno [facoltativo]</dt> <dd> Non può essere presente più di un parametro senza [<a href="optional.md"><strong>facoltativo</strong></a>] dopo l'ultimo parametro con [<strong>facoltativo</strong>] quando si usa [<a href="propput.md"><strong>propput</strong></a>], [<a href="propget.md"><strong>propget</strong></a>] o [ <a href="propputref.md"><strong>propputref</strong></a>].<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2405"></span><span id="midl2405"></span><dl> <dt><strong>MIDL2405</strong></dt> </dl></td>
<td><dl> <dt><span id="_comm_status__or__fault_status__with_pickling_requires_-Oicf"></span><span id="_comm_status__or__fault_status__with_pickling_requires_-oicf"></span><span id="_COMM_STATUS__OR__FAULT_STATUS__WITH_PICKLING_REQUIRES_-OICF"></span>[comm_status] o [fault_status] con pickling richiede -Oicf</dt> <dd> La modalità di ottimizzazione<strong>Oi</strong> precedente non supporta le procedure o i parametri con [ <a href="comm-status.md"><strong>comm_status</strong></a>] o [ <a href="fault-status.md"><strong>fault_status</strong></a>] con pickling (ovvero usando [ <a href="encode.md"><strong>encode</strong></a>] e/o [ <a href="decode.md"><strong>decode</strong></a>]).<br/> Questo avviso può essere eliminato a livello globale specificando<strong>- Oicf</strong> nella riga di comando MIDL o per una singola funzione aggiungendo l'attributo [optimize( icf:)] alla funzione nel &quot; file ACF.<br/> In generale, la modalità<strong>di ottimizzazione Oicf</strong> è consigliata rispetto alla<strong>modalità Oi.</strong><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2406"></span><span id="midl2406"></span><dl> <dt><strong>MIDL2406</strong></dt> </dl></td>
<td><dl> <dt><span id="midl_driver_and_compiler_version_mismatch"></span><span id="MIDL_DRIVER_AND_COMPILER_VERSION_MISMATCH"></span>Mancata corrispondenza tra versione del driver midl e del compilatore</dt> <dd> A Windows 2000 (MIDL versione 5.03.279) il compilatore MIDL viene implementato usando due file eseguibili: Midl.exe (driver ) e Midlc.exe (motore del compilatore). Questo errore indica che la versione di Midl.exe non corrisponde alla versione di Midlc.exe.<br/> L'errore potrebbe essere stato causato dalla copia Midl.exe ma non Midlc.exe dalla distribuzione più recente. Eseguire <strong>midl</strong> e/o <strong>midlc</strong> dalla riga di comando senza parametri per visualizzare il numero di versione del file eseguibile.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2407"></span><span id="midl2407"></span><dl> <dt><strong>MIDL2407</strong></dt> </dl></td>
<td><dl> <dt><span id="no_intermediate_file_specified__use_Midl.exe"></span><span id="no_intermediate_file_specified__use_midl.exe"></span><span id="NO_INTERMEDIATE_FILE_SPECIFIED__USE_MIDL.EXE"></span>nessun file intermedio specificato: usare Midl.exe</dt> <dd> A Windows 2000 (MIDL versione 5.03.279), il compilatore MIDL viene implementato usando due file eseguibili: Midl.exe (il driver) e Midlc.exe (motore del compilatore). Questo errore indica che Midlc.exe stato eseguito direttamente anziché usare Midl.exe.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2408"></span><span id="midl2408"></span><dl> <dt><strong>MIDL2408</strong></dt> </dl></td>
<td><dl> <dt><span id="processing_problem_with_a_parameter_in_a_procedure"></span><span id="PROCESSING_PROBLEM_WITH_A_PARAMETER_IN_A_PROCEDURE"></span>problema di elaborazione con un parametro in una procedura</dt> <dd> Questo errore può verificarsi quando si importano dati da un TLB e quando una procedura ha un parametro non valido. <br/> Se viene visualizzato questo errore, segnalare un bug a Microsoft. Specificare i file IDL, i file ACF, il file TLB e la riga di comando MIDL completa.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2409"></span><span id="midl2409"></span><dl> <dt><strong>MIDL2409</strong></dt> </dl></td>
<td><dl> <dt><span id="processing_problem_with_a_field_in_a_structure"></span><span id="PROCESSING_PROBLEM_WITH_A_FIELD_IN_A_STRUCTURE"></span>problema di elaborazione con un campo in una struttura</dt> <dd> Questo errore può verificarsi quando si importano dati da un TLB e quando una struttura ha una struttura o un campo unione non valido.<br/> Se viene visualizzato questo errore, segnalare un bug a Microsoft. Specificare i file IDL, i file ACF, il file TLB e la riga di comando MIDL completa.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2410"></span><span id="midl2410"></span><dl> <dt><strong>MIDL2410</strong></dt> </dl></td>
<td><dl> <dt><span id="internal_compiler_inconsistency_detected__the_format_string_offset_is_invalid._See_the_documentation_for_more_information."></span><span id="internal_compiler_inconsistency_detected__the_format_string_offset_is_invalid._see_the_documentation_for_more_information."></span><span id="INTERNAL_COMPILER_INCONSISTENCY_DETECTED__THE_FORMAT_STRING_OFFSET_IS_INVALID._SEE_THE_DOCUMENTATION_FOR_MORE_INFORMATION."></span>rilevata incoerenza interna del compilatore: l'offset della stringa di formato non è valido. Per altre informazioni, vedere la documentazione.</dt> <dd> Il compilatore MIDL ha rilevato un valore non valido nelle strutture di dati interne. Ciò può essere causato da strutture ricorsive o dalla violazione da parte del compilatore dei propri limiti di rappresentazione per i dati interni. Per identificare e/o risolvere il problema, provare a semplificare il file IDL. A tale scopo, è possibile semplificare i parametri complessi e le strutture di dati ricorsive o ridurre le dimensioni del file IDL suddividendo il file. Questo messaggio può essere accompagnato da una stampa diagnostica con informazioni aggiuntive sul problema.<br/> Se viene visualizzato questo errore, segnalare un bug a Microsoft. Specificare i file IDL, i file ACF, la riga di comando MIDL completa e l'eventuale output di diagnostica.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2411"></span><span id="midl2411"></span><dl> <dt><strong>MIDL2411</strong></dt> </dl></td>
<td><dl> <dt><span id="internal_compiler_inconsistency_detected__the_type_offset_is_invalid._See_the_documentation_for_more_information."></span><span id="internal_compiler_inconsistency_detected__the_type_offset_is_invalid._see_the_documentation_for_more_information."></span><span id="INTERNAL_COMPILER_INCONSISTENCY_DETECTED__THE_TYPE_OFFSET_IS_INVALID._SEE_THE_DOCUMENTATION_FOR_MORE_INFORMATION."></span>rilevata incoerenza interna del compilatore: l'offset del tipo non è valido. Per altre informazioni, vedere la documentazione.</dt> <dd> Il compilatore MIDL ha rilevato un valore non valido nelle strutture di dati interne. Ciò può essere causato da strutture ricorsive o dalla violazione da parte del compilatore dei propri limiti di rappresentazione per i dati interni. Per identificare e/o risolvere il problema, provare a semplificare il file IDL. A tale scopo, è possibile semplificare parametri complessi e strutture di dati ricorsive oppure ridurre le dimensioni del file IDL suddividendo il file. Questo messaggio può essere accompagnato da una stampa diagnostica con informazioni aggiuntive sul problema.<br/> Se viene visualizzato questo errore, segnalare un bug a Microsoft. Specificare i file IDL, i file ACF, la riga di comando MIDL completa e l'eventuale output di diagnostica.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2412"></span><span id="midl2412"></span><dl> <dt><strong>MIDL2412</strong></dt> </dl></td>
<td><dl> <dt><span id="SAFEARRAY_roo__syntax_is_not_supported_outside_of_the_library_block__use_LPSAFEARRAY_for_proxy"></span><span id="safearray_roo__syntax_is_not_supported_outside_of_the_library_block__use_lpsafearray_for_proxy"></span><span id="SAFEARRAY_ROO__SYNTAX_IS_NOT_SUPPORTED_OUTSIDE_OF_THE_LIBRARY_BLOCK__USE_LPSAFEARRAY_FOR_PROXY"></span>La sintassi SAFEARRAY(roo) non è supportata all'esterno del blocco di libreria. Usare LPSAFEARRAY per il proxy</dt> <dd> Le librerie SAFEARRAYs tipisse in modo esplicito non sono consentite all'esterno di un blocco di libreria. In alternativa, usare LPSAFEARRAY.<br/> L'esempio seguente illustra questo errore:<br/>
<pre class="syntax" data-space="preserve"><code>void roo(SAFEARRAY(long) *a); //MIDL2412 when outside a library block
void roo(LPSAFEAEEAY a);         //OK</code></pre>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2413"></span><span id="midl2413"></span><dl> <dt><strong>MIDL2413</strong></dt> </dl></td>
<td><dl> <dt><span id="bit_fields_are_not_supported"></span><span id="BIT_FIELDS_ARE_NOT_SUPPORTED"></span>I campi di bit non sono supportati</dt> <dd> I campi di bit di tipo C non sono supportati da MIDL. Questo vale per la generazione di proxy e per la generazione di TLB.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2414"></span><span id="midl2414"></span><dl> <dt><strong>MIDL2414</strong></dt> </dl></td>
<td><dl> <dt><span id="floating_point_or_complex_return_types_with__decode__are_not_supported_in_-Oicf__using_-OI"></span><span id="floating_point_or_complex_return_types_with__decode__are_not_supported_in_-oicf__using_-oi"></span><span id="FLOATING_POINT_OR_COMPLEX_RETURN_TYPES_WITH__DECODE__ARE_NOT_SUPPORTED_IN_-OICF__USING_-OI"></span>I tipi restituiti a virgola mobile o complessi con [decode] non sono supportati in -Oicf, usando -OI</dt> <dd> Le routine con tipi restituiti a virgola mobile o struttura/unione non sono supportate nel selettore di stile -Oicf. Per risolvere il problema a 32 bit, è possibile usare la modalità di ottimizzazione -Oi durante la serializzazione dei dati (usando [encode] e/o [decode]). Tuttavia, poiché l'interprete in stile -Oi precedente e il supporto per il pickling devono essere gradualmente rilasciati dopo il rilascio di Windows 2000, l'uso dei puntatori è fortemente consigliato come soluzione per questo problema. Si noti anche che in genere, la modifica di un metodo di interfaccia per l'uso di un puntatore [out, ref] anziché del valore restituito che causa il problema è completamente compatibile con le versioni precedenti in rete e può essere facilmente nascosta dal livello dell'app. <br/> Questo avviso può essere eliminato a livello globale specificando -Oi nella riga di comando MIDL o per una singola funzione aggiungendo l'attributo [optimize( i )] alla funzione nel &quot; &quot; file ACF.<br/> L'esempio seguente illustra il problema:<br/> roo.idl: <br/>
<pre class="syntax" data-space="preserve"><code>double GetDouble();</code></pre>
roo.acf: <br/>
<pre class="syntax" data-space="preserve"><code>[decode] GetDouble();</code></pre>
Un'opzione per aggirare questa limitazione è passare un parametro [out] per contenere il risultato anziché usare un valore restituito:<br/> roo.idl: <br/>
<pre class="syntax" data-space="preserve"><code>void GetDouble([out] double *result); //top level pointer is a [ref] pointer</code></pre>
roo.acf: <br/>
<pre class="syntax" data-space="preserve"><code>[decode] GetDouble();</code></pre>
Come accennato in precedenza, la soluzione descritta in precedenza è ideale non solo per le nuove interfacce, ma anche come soluzione per quelle meno recenti. La rappresentazione in transito per il nuovo argomento out è uguale a per il valore &quot; &quot; restituito (si noti void come nuovo valore restituito).<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2415"></span><span id="midl2415"></span><dl> <dt><strong>MIDL2415</strong></dt> </dl></td>
<td><dl> <dt><span id="the_return_type_is_not_supported_for_64-bit_when_using__decode_"></span><span id="THE_RETURN_TYPE_IS_NOT_SUPPORTED_FOR_64-BIT_WHEN_USING__DECODE_"></span>Il tipo restituito non è supportato per la versione a 64 bit quando si usa [decode]</dt> <dd> Le routine con tipi restituiti a virgola mobile o struttura/unione non sono supportate in modalità a 64 bit quando si esegue la serializzazione dei dati (usando [ <a href="encode.md"><strong>encode</strong></a>] e/o [ <a href="decode.md"><strong>decode</strong></a>]). Ciò è correlato al fatto che l'interprete -Oi e il serializzatore di dati di tipo precedente non sono supportati nella piattaforma a 64 bit. Per altre informazioni, vedere la descrizione di MIDL2414. <br/> L'esempio seguente illustra questo errore:<br/> roo.idl: <br/>
<pre class="syntax" data-space="preserve"><code>double GetDouble();</code></pre>
roo.acf: <br/>
<pre class="syntax" data-space="preserve"><code>[decode] GetDouble();</code></pre>
Di seguito è consigliabile risolvere il problema sia per le interfacce nuove che per le interfacce vecchie. Usare un parametro [out] per contenere il risultato invece di usare un valore restituito:<br/> roo.idl: <br/>
<pre class="syntax" data-space="preserve"><code>void GetDouble([out] double *result); //top level pointer is a [ref] pointer.</code></pre>
roo.acf: <br/>
<pre class="syntax" data-space="preserve"><code>[decode] GetDouble();</code></pre>
Si noti che questa soluzione è completamente compatibile con le versioni precedenti in transito, perché la rappresentazione di collegamento di un puntatore [ref, out] o double è uguale a quella di un double.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2416"></span><span id="midl2416"></span><dl> <dt><strong>MIDL2416</strong></dt> </dl></td>
<td><dl> <dt><span id="transmitted_type_may_not_contain_a_full_pointer_for_either__wire_marshal__or__user_marshal_"></span><span id="TRANSMITTED_TYPE_MAY_NOT_CONTAIN_A_FULL_POINTER_FOR_EITHER__WIRE_MARSHAL__OR__USER_MARSHAL_"></span>il tipo trasmesso non può contenere un puntatore completo per [wire_marshal] o [user_marshal]</dt> <dd> I tipi con attributi [ <a href="wire-marshal.md"><strong>wire_marshal</strong></a>] o [ <a href="user-marshal.md"><strong>user_marshal</strong></a>] non possono contenere puntatori completi ([ <strong>ptr</strong>]). In <a href="unique.md"><strong>alternativa, usare</strong></a>[ unique ] o [ <a href="ref.md"><strong>ref</strong></a>].<br/> L'esempio seguente illustra questo errore:<br/>
<pre class="syntax" data-space="preserve"><code>typedef struct
{
    [ptr] long *a;    //Should use [ref] or [unique] instead
}
st1;
typedef [wire_marshal(st1)] struct
{
    long a;
}
st2:
void roo(st2 *s);    //MIDL2416</code></pre>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2417"></span><span id="midl2417"></span><dl> <dt><strong>MIDL2417</strong></dt> </dl></td>
<td><dl> <dt><span id="transmitted_type_must_either_be_a_pointer_or_have_a_constant_size_for__wire_marshal__and__user_marshal_"></span><span id="TRANSMITTED_TYPE_MUST_EITHER_BE_A_POINTER_OR_HAVE_A_CONSTANT_SIZE_FOR__WIRE_MARSHAL__AND__USER_MARSHAL_"></span>il tipo trasmesso deve essere un puntatore o avere una dimensione costante per [wire_marshal] e [user_marshal]</dt> <dd> I tipi di primo livello con attributi [ <a href="wire-marshal.md"><strong>wire_marshal</strong></a>] o [ <a href="user-marshal.md"><strong>user_marshal</strong></a>] devono avere dimensioni ben definite in fase di compilazione. Non possono essere o contenere matrici conformi o di dimensioni variabili.<br/> L'esempio seguente illustra questo errore:<br/>
<pre class="syntax" data-space="preserve"><code>typedef struct        //Type contains variable-sized array
{
    long s;
    [size_is(s)] char a[];
}
st1;
typedef [wire_marshal(st1)] struct
{
    long a;
}
st2;
void roo(st2 *s);        //MIDL2417</code></pre>
</dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2418"></span><span id="midl2418"></span><dl> <dt><strong>MIDL2418</strong></dt> </dl></td>
<td><dl> <dt><span id="procedures_with__propget__must_have_at_least_one_parameter_or_a_return_value"></span><span id="PROCEDURES_WITH__PROPGET__MUST_HAVE_AT_LEAST_ONE_PARAMETER_OR_A_RETURN_VALUE"></span>Le routine con [propget] devono avere almeno un parametro o un valore restituito</dt> <dd> Le routine con l'attributo [propget] devono avere un modo per restituire il valore della proprietà. Devono avere almeno un parametro [<a href="-out.md"><strong>out</strong></a>] o un valore restituito.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL2461"></span><span id="midl2461"></span><dl> <dt><strong>MIDL2461</strong></dt> </dl></td>
<td><dl> <dt><span id="The__readonly__attribute_was_applied_at_the_method_level."></span><span id="the__readonly__attribute_was_applied_at_the_method_level."></span><span id="THE__READONLY__ATTRIBUTE_WAS_APPLIED_AT_THE_METHOD_LEVEL."></span>L'attributo [readonly] è stato applicato a livello di metodo.</dt> <dd> L'attributo [readonly] può essere applicato solo a livello di parametro.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="MIDL2465"></span><span id="midl2465"></span><dl> <dt><strong>MIDL2465</strong></dt> </dl></td>
<td><dl> <dt><span id="Structures_containing_conformant_arrays_must_be_passed_by_reference"></span><span id="structures_containing_conformant_arrays_must_be_passed_by_reference"></span><span id="STRUCTURES_CONTAINING_CONFORMANT_ARRAYS_MUST_BE_PASSED_BY_REFERENCE"></span>Le strutture contenenti matrici conformi devono essere passate per riferimento</dt> <dd> I parametri di primo livello in RPC devono avere una dimensione ben definita in fase di compilazione. Non possono essere né contenere matrici conformi o di dimensioni variabili. Inoltre, gli utenti non possono codificare/decodificare un tipo senza dimensioni ben definite. Le applicazioni devono passare uno struct conforme o uno struct variabile conforme per riferimento.<br/> L'esempio seguente illustra questo errore:<br/>
<pre class="syntax" data-space="preserve"><code>typedef struct        //Type contains variable-sized array
{
    long s;
    [size_is(s)] char a[];
}
st1;
void roo(st1 s);        //MIDL2465
 
on .acf file
typedef [encode,decode] st1; //MIDL2465</code></pre>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><span id="MIDL9008"></span><span id="midl9008"></span><dl> <dt><strong>MIDL9008</strong></dt> </dl></td>
<td><dl> <dt><span id="_internal_compiler_problem__system_error_code__-_the_compiler_cannot_continue_for_an_unknown_reason._See_documentation_for_a_workaround."></span><span id="_internal_compiler_problem__system_error_code__-_the_compiler_cannot_continue_for_an_unknown_reason._see_documentation_for_a_workaround."></span><span id="_INTERNAL_COMPILER_PROBLEM__SYSTEM_ERROR_CODE__-_THE_COMPILER_CANNOT_CONTINUE_FOR_AN_UNKNOWN_REASON._SEE_DOCUMENTATION_FOR_A_WORKAROUND."></span> problema interno del <system error code> - compilatore. Il compilatore non può continuare per un motivo sconosciuto. Per una soluzione alternativa, vedere la documentazione.</dt> <dd> Il compilatore non è stato in grado di continuare e la causa dell'errore è sconosciuta. Il numero di errore esadecimale è un identificatore di errore di sistema. La compilazione potrebbe non essere riuscita a causa di un problema esterno, ad esempio una condizione di memoria insufficiente. In tal caso, è possibile trovare altre informazioni in Winerror.h o Ntstatus.h. <br/> Questo errore viene in genere generato in due situazioni:<br/>
<ul>
<li>Il compilatore MIDL non è riuscito a eseguire il ripristino dopo aver rilevato un errore nel file IDL. Se MIDL ha restituito messaggi di errore relativi al file IDL, provare a correggerli e a ricompilare. Se non sono presenti messaggi di errore, è possibile che il compilatore abbia avuto esito negativo prima di poter segnalare un errore. Cercare un errore di sintassi nella riga per cui viene segnalato l'errore interno del compilatore.</li>
<li>Il compilatore MIDL non è stato in grado di generare codice corretto con un'opzione di ottimizzazione specificata. Provare a modificare le modalità del compilatore, a compilare l'ottimizzazione in modalità mista<a href="-os.md"><strong>(/Os)</strong></a>o a rimuovere tutte le ottimizzazioni. In caso contrario, ricompilare usando il flag /NO_FORMAT_OPT per eliminare l'ottimizzazione predefinita di MIDL dei descrittori di procedure e tipi.</li>
</ul>
In alcuni casi questo errore si verifica anche quando il file IDL è corretto e non vengono usate opzioni di ottimizzazione. In questo caso, provare a riscrivere la sezione di codice nelle vicinanze della posizione in cui è stato segnalato l'errore rimuovendo eventuali modifiche recenti, semplificando o ridisposizione dei tipi di dati, modificando i prototipi oppure iniziando a impostare come commento parti del file IDL per individuare il codice del problema.<br/> Se nessuna di queste opzioni funziona o se si pensa che il problema possa essere correlato a un bug in Midl.exe, inviare una notifica a Microsoft, fornendo tutti i dettagli pertinenti.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



 

