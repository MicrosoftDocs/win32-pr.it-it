---
description: La tabella RemoveRegistry contiene le informazioni del registro di sistema che l'applicazione deve eliminare dal registro di sistema.
ms.assetid: 8be382f1-f5ab-4a9d-bf0e-05275310c5b5
title: Tabella RemoveRegistry
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8de39edd15484ac4bcda675ec8bffaca0540a0ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967736"
---
# <a name="removeregistry-table"></a>Tabella RemoveRegistry

La tabella RemoveRegistry contiene le informazioni del registro di sistema che l'applicazione deve eliminare dal registro di sistema.

La tabella RemoveRegistry include le colonne seguenti.



| Colonna         | Tipo                         | Chiave | Nullable |
|----------------|------------------------------|-----|----------|
| RemoveRegistry | [Identificatore](identifier.md) | S   | N        |
| Radice           | [Integer](integer.md)       | N   | N        |
| Chiave            | [RegPath](regpath.md)       | N   | N        |
| Nome           | [Formattato](formatted.md)   | N   | S        |
| Componente\_    | [Identificatore](identifier.md) | N   | N        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="RemoveRegistry"></span><span id="removeregistry"></span><span id="REMOVEREGISTRY"></span>RemoveRegistry
</dt> <dd>

Chiave per questa tabella.

</dd> <dt>

<span id="Root"></span><span id="root"></span><span id="ROOT"></span>Radice
</dt> <dd>

Chiave radice predefinita per il valore del registro di sistema.



| Costante                          | Valore esadecimale | Decimal | Chiave radice                                                                                                                                                                                                           |
|-----------------------------------|-------------|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| (nessuna)                            | \- 0x001    | -1      | **HKEY \_ Il programma di installazione \_ dell'utente corrente** imposta questa chiave durante l'installazione per utente.<br/>                                                                                                                    |
| (nessuna)                            | -0x001      | -1      | **HKEY \_ Il programma di installazione del \_ computer locale** imposta questa chiave durante l'installazione di tutti gli utenti con [**ALLUSERS**](allusers.md) impostato su 1.<br/>                                                                       |
| **msidbRegistryRootClassesRoot**  | 0x000       | 0       | **HKEY \_ \_Radice classi** il programma di installazione rimuove il valore **da \\ HKCU Software \\ Classes** hive durante le installazioni nel [contesto di installazione](installation-context.md)per utente e per computer.<br/> |
| **msidbRegistryRootCurrentUser**  | 0x001       | 1       | **HKEY \_ \_ utente corrente**                                                                                                                                                                                            |
| **msidbRegistryRootLocalMachine** | 0x002       | 2       | **\_computer locale \_ HKEY**                                                                                                                                                                                           |
| **msidbRegistryRootUsers**        | 0x003       | 3       | **\_utenti HKEY**                                                                                                                                                                                                    |



 

</dd> <dt>

<span id="Key"></span><span id="key"></span><span id="KEY"></span>Chiave
</dt> <dd>

Chiave localizzabile per il valore del registro di sistema.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nome
</dt> <dd>

Nome del valore del registro di sistema localizzabile.

La stringa seguente nella colonna Name ha un significato speciale.



| string | Significato                                                                                                    |
|--------|------------------------------------------------------------------------------------------------------------|
| "-"    | La chiave deve essere eliminata, se presente, con tutti i relativi valori e sottochiavi, quando viene installato il componente. |



 

Si noti che la [tabella del registro di sistema](registry-table.md) deve essere utilizzata per creare o rimuovere una chiave del registro di sistema quando il componente viene rimosso.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Chiave esterna nella prima colonna della tabella dei [componenti](component-table.md) che fa riferimento al componente che controlla l'eliminazione del valore del registro di sistema.

</dd> </dl>

## <a name="remarks"></a>Commenti

Le informazioni del registro di sistema vengono eliminate dal registro di sistema quando il componente corrispondente è stato selezionato per l'installazione locale o per l'esecuzione dall'origine.

Questa tabella viene definita quando viene eseguita l' [azione RemoveRegistryValues](removeregistryvalues-action.md) .

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE46](ice46.md)  
[ICE69](ice69.md)  
</dl>

 

 




