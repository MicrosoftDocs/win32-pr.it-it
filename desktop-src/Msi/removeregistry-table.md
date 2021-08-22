---
description: La tabella RemoveRegistry contiene le informazioni del Registro di sistema che l'applicazione deve eliminare dal Registro di sistema.
ms.assetid: 8be382f1-f5ab-4a9d-bf0e-05275310c5b5
title: Tabella RemoveRegistry
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 170dc727eef47ac214f7a7f42af7f487f53ad0b9a0658182420b28eb5224e38d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119314881"
---
# <a name="removeregistry-table"></a>Tabella RemoveRegistry

La tabella RemoveRegistry contiene le informazioni del Registro di sistema che l'applicazione deve eliminare dal Registro di sistema.

La tabella RemoveRegistry contiene le colonne seguenti.



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

Chiave radice predefinita per il valore del Registro di sistema.



| Costante                          | Valore esadecimale | Decimal | Chiave radice                                                                                                                                                                                                           |
|-----------------------------------|-------------|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| (nessuna)                            | \- 0x001    | -1      | **HKEY \_ CURRENT \_ USER** Installer imposta questa chiave durante un'installazione per utente.<br/>                                                                                                                    |
| (nessuna)                            | -0x001      | -1      | **HKEY \_ Local \_ MACHINE** Installer imposta questa chiave durante l'installazione di tutti gli utenti con [**ALLUSERS**](allusers.md) impostato su 1.<br/>                                                                       |
| **msidbRegistryRootClassesRoot**  | 0x000       | 0       | **HKEY \_ CLASSES \_ ROOT** Il programma di installazione rimuove il valore dall'hive **HKCU \\ Software \\ Classes** durante le installazioni nel contesto di installazione per utente e per [computer.](installation-context.md)<br/> |
| **msidbRegistryRootCurrentUser**  | 0x001       | 1       | **HKEY \_ CURRENT \_ USER**                                                                                                                                                                                            |
| **msidbRegistryRootLocalMachine** | 0x002       | 2       | **HKEY \_ LOCAL \_ MACHINE**                                                                                                                                                                                           |
| **msidbRegistryRootUsers**        | 0x003       | 3       | **UTENTI \_ HKEY**                                                                                                                                                                                                    |



 

</dd> <dt>

<span id="Key"></span><span id="key"></span><span id="KEY"></span>Chiave
</dt> <dd>

Chiave localizzabile per il valore del Registro di sistema.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nome
</dt> <dd>

Nome del valore localizzabile del Registro di sistema.

La stringa seguente nella colonna Name ha un significato speciale.



| string | Significato                                                                                                    |
|--------|------------------------------------------------------------------------------------------------------------|
| "-"    | La chiave deve essere eliminata, se presente, con tutti i relativi valori e sottochiavi, quando il componente viene installato. |



 

Si noti che [la tabella Registry](registry-table.md) deve essere usata per creare o rimuovere una chiave del Registro di sistema quando il componente viene rimosso.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Chiave esterna nella prima colonna della tabella [Component](component-table.md) che fa riferimento al componente che controlla l'eliminazione del valore del Registro di sistema.

</dd> </dl>

## <a name="remarks"></a>Commenti

Le informazioni del Registro di sistema vengono eliminate dal Registro di sistema quando il componente corrispondente è stato selezionato per l'installazione locale o l'esecuzione dall'origine.

Questa tabella viene indicata quando viene eseguita [l'azione RemoveRegistryValues.](removeregistryvalues-action.md)

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE46](ice46.md)  
[ICE69](ice69.md)  
</dl>

 

 




