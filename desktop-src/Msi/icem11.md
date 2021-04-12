---
description: ICEM11 verifica che un modulo merge configurabile elenchi la tabella ModuleConfiguration e la tabella ModuleSubstitution nella tabella ModuleIgnoreTable del modulo.
ms.assetid: f0199137-0a40-40ca-b3cf-ff8eef4309cc
title: ICEM11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 403a36435ce2367fc356934740e6d022f5457698
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232444"
---
# <a name="icem11"></a>ICEM11

ICEM11 verifica che un modulo merge configurabile elenchi la tabella [ModuleConfiguration](moduleconfiguration-table.md) e la [tabella ModuleSubstitution](modulesubstitution-table.md) nella [tabella ModuleIgnoreTable](moduleignoretable-table.md) del modulo. In questo modo si garantisce che gli strumenti di merge che non riconoscono i moduli unione configurabili (minori della versione 2,0) non copino queste tabelle nel database di destinazione.

Questo ICEM è disponibile nel file Mergemod. cub fornito in Windows Installer SDK 2,0 e versioni successive. Per informazioni dettagliate, vedere [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).

## <a name="result"></a>Risultato

ICEM11 Invia un errore se il modulo contiene una tabella ModuleConfiguration o ModuleSubstitution non elencata nella tabella ModuleIgnoreTable.

## <a name="example"></a>Esempio

ICEM11 invia i messaggi di errore seguenti per un modulo contenente le voci di database indicate di seguito.

``` syntax
Error The module contains a ModuleConfiguration or ModuleSubstitution 
table. These tables must be listed in the ModuleIgnoreTable table.
```

[ModuleConfiguration](moduleconfiguration-table.md) (parziale)



| Nome     | Formato | Tipo   | ContextData | DefaultValue |
|----------|--------|--------|-------------|--------------|
| IconKey1 | 1      | Binary | Icona        | DefaultIcon  |



 

[ModuleSubstitution](modulesubstitution-table.md)



| Tabella   | Riga              | Colonna | valore        |
|---------|------------------|--------|--------------|
| Control | Dialog1; Control1 | Testo   | \[IconKey1\] |



 

[ModuleIgnoreTable](moduleignoretable-table.md)



| Tabella               |
|---------------------|
| ModuleConfiguration |



 

Per correggere l'errore, includere entrambe le tabelle ModuleSubstitution e ModuleConfiguration nella tabella ModuleIgnoreTable.

## <a name="table-used-during-execution"></a>Tabella utilizzata durante l'esecuzione

[ModuleSubstitution](modulesubstitution-table.md)

[ModuleConfiguration](moduleconfiguration-table.md)

[ModuleIgnoreTable](moduleignoretable-table.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio del modulo merge](merge-module-ice-reference.md)
</dt> </dl>

 

 



