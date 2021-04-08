---
description: La tabella del registro di sistema include le informazioni del registro di sistema che l'applicazione deve impostare nel registro di sistema.
ms.assetid: 809ffd02-cf97-42d8-aed9-c13a14dcd8b4
title: Tabella del registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b16cb2084716ea8cb9830056808e9c6be7da667f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967408"
---
# <a name="registry-table"></a>Tabella del registro di sistema

La tabella del registro di sistema include le informazioni del registro di sistema che l'applicazione deve impostare nel registro di sistema.

La tabella del registro di sistema contiene le colonne seguenti.



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

<span id="Registry"></span><span id="registry"></span><span id="REGISTRY"></span>Del registro
</dt> <dd>

Chiave primaria utilizzata per identificare un record del registro di sistema.

</dd> <dt>

<span id="Root"></span><span id="root"></span><span id="ROOT"></span>Radice
</dt> <dd>

Chiave radice predefinita per il valore del registro di sistema. Immettere un valore pari a-1 in questo campo per fare in modo che la chiave radice dipenda dal tipo di installazione. Immettere uno degli altri valori nella tabella seguente per forzare la scrittura del valore del registro di sistema in una particolare chiave radice.



| Costante                          | Valore esadecimale | Decimal | Chiave radice                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------|-------------|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| (nessuna)                            | \- 0x001    | -1      | Se si tratta di un'installazione per utente, il valore del registro di sistema viene scritto in **HKEY \_ Current \_ User**. Se si tratta di un'installazione per computer, il valore del registro di sistema viene scritto in **HKEY \_ Local \_ Machine**. Si noti che un'installazione per computer viene specificata impostando la proprietà [**ALLUSERS**](allusers.md) su 1.<br/>                |
| **msidbRegistryRootClassesRoot**  | 0x000       | 0       | **HKEY \_ CLASSI \_ radice** il programma di installazione scrive o rimuove il valore da **HKCU \\ software \\ Classes** hive durante l'installazione nel [contesto di installazione](installation-context.md)per utente.<br/> Il programma di installazione scrive o rimuove il valore dall'hive **\\ \\ classi Software HKLM** durante le installazioni per computer.<br/> |
| **msidbRegistryRootCurrentUser**  | 0x001       | 1       | **HKEY \_ \_ utente corrente**                                                                                                                                                                                                                                                                                                                      |
| **msidbRegistryRootLocalMachine** | 0x002       | 2       | **\_computer locale \_ HKEY**                                                                                                                                                                                                                                                                                                                     |
| **msidbRegistryRootUsers**        | 0x003       | 3       | **\_utenti HKEY**                                                                                                                                                                                                                                                                                                                              |



 

Si noti che è consigliabile che le voci del registro di sistema scritte nell'hive **HKCU** facciano riferimento a un componente con il bit RegistryKeyPath impostato nella colonna Attributes della [tabella Component](component-table.md). Ciò garantisce che il programma di installazione scriva le voci del registro di sistema necessarie quando sono presenti più utenti nello stesso computer.

</dd> <dt>

<span id="Key"></span><span id="key"></span><span id="KEY"></span>Chiave
</dt> <dd>

Chiave localizzabile per il valore del registro di sistema.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nome
</dt> <dd>

Questa colonna contiene il nome del valore del registro di sistema (localizzabile). Se è null, i dati immessi nella colonna valore vengono scritti nella chiave del registro di sistema predefinita.

Se la colonna valore è null, le stringhe mostrate nella tabella seguente nella colonna Name hanno un significato speciale.



| string | Significato                                                                                                                                                                                          |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \+     | La chiave deve essere creata, se assente, durante l'installazione del componente.                                                                                                                            |
| \-     | La chiave deve essere eliminata, se presente, con tutti i relativi valori e sottochiavi, quando viene disinstallato il componente.                                                                                     |
| \*     | La chiave deve essere creata, se assente, durante l'installazione del componente. Inoltre, la chiave deve essere eliminata, se presente, con tutti i relativi valori e sottochiavi quando il componente viene disinstallato. |



 

Si noti che è necessario usare la [tabella RemoveRegistry](removeregistry-table.md) se è necessario eliminare una chiave del registro di sistema installata, con i relativi valori e sottochiavi, quando viene installato il componente.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valore
</dt> <dd>

Questa colonna è il valore del registro di sistema localizzabile. Il campo è [formattato](formatted.md). Se il valore è collegato a uno dei seguenti prefissi (ovvero \# % *valore*), il valore viene interpretato come descritto nella tabella. Si noti che ogni prefisso inizia con un simbolo di cancelletto ( \# ). Se il valore inizia con due o più segni di cancelletto consecutivi ( \# ), il primo \# viene ignorato e il valore viene interpretato e archiviato come stringa.



| Prefisso | Significato                                                                        |
|--------|--------------------------------------------------------------------------------|
| \#x    | Il valore viene interpretato e archiviato come valore esadecimale (REG \_ Binary).      |
| \#%    | Il valore viene interpretato e archiviato come stringa espandibile (REG \_ expand \_ SZ). |
| \#     | Il valore viene interpretato e archiviato come Integer (REG \_ DWORD).                |



 

-   Se il valore contiene la tilde della sequenza \[ ~ \] , il valore viene interpretato come un elenco di stringhe delimitato da valori null ( \_ reg \_ multisz). Per specificare, ad esempio, un elenco contenente le tre stringhe a, b e c, utilizzare "a \[ ~ \] b \[ ~ \] c".
-   La sequenza \[ ~ \] all'interno del valore separa le singole stringhe e viene interpretata e archiviata come carattere null.
-   Se un oggetto \[ ~ \] precede l'elenco di stringhe, le stringhe devono essere aggiunte alle stringhe dei valori del registro di sistema esistenti. Se nel valore del registro di sistema è già presente una stringa di Accodamento, viene rimossa l'occorrenza originale della stringa.
-   Se un oggetto \[ ~ \] segue la fine dell'elenco di stringhe, le stringhe devono essere antepone alle stringhe dei valori del registro di sistema esistenti. Se una stringa in sospeso si trova già nel valore del registro di sistema, viene rimossa l'occorrenza originale della stringa.
-   Se un oggetto \[ ~ \] si trova sia all'inizio che alla fine o all'inizio o alla fine dell'elenco di stringhe, le stringhe devono sostituire tutte le stringhe del valore del registro di sistema esistenti.
-   In caso contrario, il valore viene interpretato e archiviato come stringa (REG \_ SZ).

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Chiave esterna nella prima colonna della tabella dei [componenti](component-table.md) che fa riferimento al componente che controlla l'installazione del valore del registro di sistema.

</dd> </dl>

## <a name="remarks"></a>Commenti

Le azioni [WriteRegistryValori consente](writeregistryvalues-action.md) e [RemoveRegistryValues](removeregistryvalues-action.md) nelle [*tabelle di sequenza*](s-gly.md) elaborano le informazioni contenute in questa tabella. Per informazioni sull'utilizzo di *tabelle di sequenza*, vedere [utilizzo di una tabella di sequenza](using-a-sequence-table.md).

Le informazioni del registro di sistema vengono scritte nel registro di sistema quando il componente corrispondente è stato selezionato per l'installazione locale o per l'esecuzione dall'origine.

Si noti che il programma di installazione rimuove una chiave del registro di sistema dopo la rimozione dell'ultimo valore o della sottochiave sotto la chiave. Per evitare la rimozione di una chiave del registro di sistema vuota durante la disinstallazione di, scrivere un valore fittizio sotto la chiave che deve essere mantenuta e immettere + nella colonna nome. Se \* è nella colonna nome, la chiave viene eliminata con tutti i relativi valori e sottochiavi quando il componente viene rimosso.

È possibile utilizzare un'azione personalizzata per aggiungere righe alla tabella del registro di sistema durante un'installazione, una disinstallazione o una transazione di ripristino. Queste righe non vengono mantenute nella tabella del registro di sistema e le informazioni sono disponibili solo durante la transazione corrente. L'azione personalizzata deve pertanto essere eseguita in ogni installazione, disinstallazione o ripristino della transazione che richiede le informazioni contenute in queste righe aggiuntive. L'azione personalizzata deve precedere le azioni [RemoveRegistryValues](removeregistryvalues-action.md) e [WriteRegistryValori consente](writeregistryvalues-action.md) nella sequenza di azione.

Per informazioni su come proteggere una chiave del registro di sistema, vedere la [tabella MsiLockPermissionsEx](msilockpermissionsex-table.md) e la [tabella LockPermissions](lockpermissions-table.md).

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

 

 




