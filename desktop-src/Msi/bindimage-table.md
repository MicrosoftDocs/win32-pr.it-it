---
description: La tabella BindImage contiene informazioni su ogni eseguibile o DLL che deve essere associato alle DLL importate.
ms.assetid: 68bf064c-dd85-4796-8e08-6af307f94ad8
title: Tabella BindImage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 729ae4f36f3b258845bcba13748495dc9dfb53c86268bd61e98475d1c7c0c282
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119500767"
---
# <a name="bindimage-table"></a>Tabella BindImage

La tabella BindImage contiene informazioni su ogni eseguibile o DLL che deve essere associato alle DLL importate.

La tabella BindImage include le colonne seguenti.



| Colonna | Tipo                         | Chiave | Nullable |
|--------|------------------------------|-----|----------|
| file\_ | [Identificatore](identifier.md) | S   | N        |
| Percorso   | [Percorsi](paths.md)           | N   | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_
</dt> <dd>

Una chiave esterna alla colonna uno della [tabella File](file-table.md). Deve trattarsi di un file eseguibile o di un file DLL.

</dd> <dt>

<span id="Path"></span><span id="path"></span><span id="PATH"></span>Percorso
</dt> <dd>

Elenco di percorsi, separati da punti e virgola, che rappresentano i percorsi in cui eseguire la ricerca per trovare le DLL importate. L'elenco è in genere un elenco di proprietà, con ogni proprietà racchiusa tra parentesi quadre ( \[ \] ) .

</dd> </dl>

## <a name="remarks"></a>Commenti

Il programma di installazione calcola l'indirizzo virtuale di ogni funzione importata da tutte le DLL e l'indirizzo virtuale calcolato viene quindi salvato nella tabella di indirizzi di importazione (IAT) dell'immagine di importazione.

Questa tabella viene indicata quando viene eseguita [l'azione BindImage.](bindimage-action.md)

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE46](ice46.md)  
[ICE76](ice76.md)  
</dl>

 

 



