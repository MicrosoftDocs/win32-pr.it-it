---
description: La tabella azione BindImage sul contiene informazioni su ogni file eseguibile o DLL che deve essere associato alle DLL importate.
ms.assetid: 68bf064c-dd85-4796-8e08-6af307f94ad8
title: Tabella azione BindImage sul
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f47b97efc8886d7748d0426a49ed76567810939c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967254"
---
# <a name="bindimage-table"></a>Tabella azione BindImage sul

La tabella azione BindImage sul contiene informazioni su ogni file eseguibile o DLL che deve essere associato alle DLL importate.

La tabella azione BindImage sul include le colonne seguenti.



| Colonna | Tipo                         | Chiave | Nullable |
|--------|------------------------------|-----|----------|
| file\_ | [Identificatore](identifier.md) | S   | N        |
| Percorso   | [Percorsi](paths.md)           | N   | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_
</dt> <dd>

Chiave esterna per la colonna uno della [tabella dei file](file-table.md). Deve trattarsi di un file eseguibile o di un file DLL.

</dd> <dt>

<span id="Path"></span><span id="path"></span><span id="PATH"></span>Percorso
</dt> <dd>

Elenco di percorsi, separati da punti e virgola, che rappresentano i percorsi in cui eseguire la ricerca per trovare le dll importate. L'elenco è in genere un elenco di proprietà, con ogni proprietà racchiusa tra parentesi quadre ( \[ \] ).

</dd> </dl>

## <a name="remarks"></a>Commenti

Il programma di installazione calcola l'indirizzo virtuale di ogni funzione importata da tutte le dll e l'indirizzo virtuale calcolato viene quindi salvato nella tabella degli indirizzi di importazione (IAT) dell'immagine di importazione.

Questa tabella viene definita quando viene eseguita l' [azione azione BindImage sul](bindimage-action.md) .

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE46](ice46.md)  
[ICE76](ice76.md)  
</dl>

 

 



