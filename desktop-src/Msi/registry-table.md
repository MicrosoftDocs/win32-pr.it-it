---
description: La tabella Registry contiene le informazioni del Registro di sistema che l'applicazione deve impostare nel Registro di sistema.
ms.assetid: 809ffd02-cf97-42d8-aed9-c13a14dcd8b4
title: Tabella del Registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6b76fbc52357cdba68dfdcdda37e6edb3032086bf101788db0cdc69c0281264
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128991"
---
# <a name="registry-table"></a>Tabella del Registro di sistema

La tabella Registry contiene le informazioni del Registro di sistema che l'applicazione deve impostare nel Registro di sistema.

La tabella Registry contiene le colonne seguenti.



| Colonna      | Tipo                         | Chiave | Nullable |
|-------------|------------------------------|-----|----------|
| Registro    | [Identificatore](identifier.md) | S   | N        |
| Radice        | [Integer](integer.md)       | N   | N        |
| Chiave         | [RegPath](regpath.md)       | N   | N        |
| Nome        | [Formattato](formatted.md)   | N   | S        |
| Valore       | [Formattato](formatted.md)   | N   | S        |
| Componente\_ | [Identificatore](identifier.md) | N   | N        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Registry"></span><span id="registry"></span><span id="REGISTRY"></span>Registro
</dt> <dd>

Chiave primaria usata per identificare un record del Registro di sistema.

</dd> <dt>

<span id="Root"></span><span id="root"></span><span id="ROOT"></span>Radice
</dt> <dd>

Chiave radice predefinita per il valore del Registro di sistema. Immettere il valore -1 in questo campo per rendere la chiave radice dipendente dal tipo di installazione. Immettere uno degli altri valori nella tabella seguente per forzare la scrittura del valore del Registro di sistema in una chiave radice specifica.



| Costante                          | Valore esadecimale | Decimal | Chiave radice                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------|-------------|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| (nessuna)                            | \- 0x001    | -1      | Se si tratta di un'installazione per utente, il valore del Registro di sistema viene scritto in **HKEY \_ CURRENT \_ USER**. Se si tratta di un'installazione per computer, il valore del Registro di sistema viene scritto in **HKEY \_ LOCAL \_ MACHINE**. Si noti che viene specificata un'installazione per computer impostando la [**proprietà ALLUSERS**](allusers.md) su 1.<br/>                |
| **msidbRegistryRootClassesRoot**  | 0x000       | 0       | **HKEY \_ CLASSES \_ ROOT** Il programma di installazione scrive o rimuove il valore dall'hive **HKCU \\ Software \\ Classes** durante l'installazione nel contesto di installazione per [utente](installation-context.md).<br/> Il programma di installazione scrive o rimuove il valore dall'hive **HKLM \\ Software \\ Classes** durante le installazioni per computer.<br/> |
| **msidbRegistryRootCurrentUser**  | 0x001       | 1       | **HKEY \_ CURRENT \_ USER**                                                                                                                                                                                                                                                                                                                      |
| **msidbRegistryRootLocalMachine** | 0x002       | 2       | **HKEY \_ LOCAL \_ MACHINE**                                                                                                                                                                                                                                                                                                                     |
| **msidbRegistryRootUsers**        | 0x003       | 3       | **UTENTI \_ HKEY**                                                                                                                                                                                                                                                                                                                              |



 

Si noti che è consigliabile che le voci del Registro di sistema scritte nell'hive **HKCU** fanno riferimento a un componente con il bit RegistryKeyPath impostato nella colonna Attributi della [tabella Component](component-table.md). Ciò garantisce che il programma di installazione scrive le voci del Registro di sistema necessarie quando sono presenti più utenti nello stesso computer.

</dd> <dt>

<span id="Key"></span><span id="key"></span><span id="KEY"></span>Chiave
</dt> <dd>

Chiave localizzabile per il valore del Registro di sistema.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nome
</dt> <dd>

Questa colonna contiene il nome del valore del Registro di sistema (localizzabile). Se è Null, i dati immessi nella colonna Valore vengono scritti nella chiave del Registro di sistema predefinita.

Se la colonna Value è Null, le stringhe mostrate nella tabella seguente nella colonna Name hanno un significato speciale.



| string | Significato                                                                                                                                                                                          |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \+     | La chiave deve essere creata, se assente, quando viene installato il componente.                                                                                                                            |
| \-     | La chiave deve essere eliminata, se presente, con tutti i relativi valori e sottochiavi, quando il componente viene disinstallato.                                                                                     |
| \*     | La chiave deve essere creata, se assente, quando viene installato il componente. Inoltre, la chiave deve essere eliminata, se presente, con tutti i relativi valori e sottochiavi, quando il componente viene disinstallato. |



 

Si noti che è necessario usare la tabella [RemoveRegistry](removeregistry-table.md) se è necessario eliminare una chiave del Registro di sistema installata, con i relativi valori e sottochiavi, quando il componente viene installato.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valore
</dt> <dd>

Questa colonna è il valore localizzabile del Registro di sistema. Il campo è [formattato.](formatted.md) Se il valore è collegato a uno dei prefissi seguenti (ad esempio, value ), il valore viene interpretato come \# % descritto nella tabella. Si noti che ogni prefisso inizia con un simbolo di numero ( \# ). Se il valore inizia con due o più simboli di numero consecutivi ( ), il primo viene ignorato e il valore viene interpretato e \# \# archiviato come stringa.



| Prefisso | Significato                                                                        |
|--------|--------------------------------------------------------------------------------|
| \#X    | Il valore viene interpretato e archiviato come valore esadecimale (REG \_ BINARY).      |
| \#%    | Il valore viene interpretato e archiviato come stringa espandibile (REG \_ EXPAND \_ SZ). |
| \#     | Il valore viene interpretato e archiviato come intero (REG \_ DWORD).                |



 

-   Se il valore contiene la sequenza tilde , il valore viene interpretato come un elenco di stringhe delimitato da \[ ~ \] Null (REG \_ MULTI \_ SZ). Ad esempio, per specificare un elenco contenente le tre stringhe a, b e c, usare "a \[ ~ \] b \[ ~ \] c".
-   La sequenza \[ ~ \] all'interno del valore separa le singole stringhe e viene interpretata e archiviata come carattere Null.
-   Se \[ ~ precede l'elenco di stringhe, le stringhe devono essere aggiunte a tutte le stringhe di valori del Registro \] di sistema esistenti. Se nel valore del Registro di sistema è già presente una stringa di accodamento, l'occorrenza originale della stringa viene rimossa.
-   Se un oggetto segue la fine dell'elenco di stringhe, le stringhe devono essere \[ ~ anteposte a tutte le stringhe di valori del Registro \] di sistema esistenti. Se nel valore del Registro di sistema è già presente una stringa anteponente, l'occorrenza originale della stringa viene rimossa.
-   Se un \[ ~ è all'inizio e alla fine o non all'inizio né alla fine dell'elenco di stringhe, le stringhe sostituiscono le stringhe dei valori del Registro \] di sistema esistenti.
-   In caso contrario, il valore viene interpretato e archiviato come stringa (REG \_ SZ).

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Chiave esterna nella prima colonna della tabella [Componente](component-table.md) che fa riferimento al componente che controlla l'installazione del valore del Registro di sistema.

</dd> </dl>

## <a name="remarks"></a>Commenti

Le [azioni WriteRegistryValues](writeregistryvalues-action.md) [e RemoveRegistryValues](removeregistryvalues-action.md) nelle tabelle [*di sequenza*](s-gly.md) elaborano le informazioni in questa tabella. Per informazioni sull'uso *delle tabelle di sequenza,* vedere [Uso di una tabella di sequenza](using-a-sequence-table.md).

Le informazioni del Registro di sistema vengono scritte nel Registro di sistema quando il componente corrispondente è stato selezionato per l'installazione locale o l'esecuzione dall'origine.

Si noti che il programma di installazione rimuove una chiave del Registro di sistema dopo la rimozione dell'ultimo valore o della sottochiave sotto la chiave. Per impedire la rimozione di una chiave del Registro di sistema vuota durante la disinstallazione, scrivere un valore fittizio nella chiave da mantenere e immettere + nella colonna Nome. Se si trova nella colonna Nome, la chiave viene eliminata, con tutti i relativi valori e \* sottochiavi, quando il componente viene rimosso.

È possibile usare un'azione personalizzata per aggiungere righe alla tabella Del Registro di sistema durante una transazione di installazione, disinstallazione o ripristino. Queste righe non vengono mantenute nella tabella Registro di sistema e le informazioni sono disponibili solo durante la transazione corrente. L'azione personalizzata deve quindi essere eseguita in ogni transazione di installazione, disinstallazione o ripristino che richiede le informazioni in queste righe aggiuntive. L'azione personalizzata deve essere eseguita prima [delle azioni RemoveRegistryValues](removeregistryvalues-action.md) e [WriteRegistryValues](writeregistryvalues-action.md) nella sequenza di azioni.

Per informazioni su come proteggere una chiave del Registro di sistema, vedere la tabella [MsiLockPermissionsEx](msilockpermissionsex-table.md) e [la tabella LockPermissions](lockpermissions-table.md).

## <a name="validation"></a>Convalida

<dl>

[ICE02](ice02.md)  
[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE38](ice38.md)  
[ICE43](ice43.md)  
[ICE46](ice46.md)  
[ICE49](ice49.md)  
[ICE53](ice53.md)  
[ICE55](ice55.md)  
[ICE57](ice57.md)  
[ICE70](ice70.md)  
[ICE80](ice80.md)  
</dl>

 

 




