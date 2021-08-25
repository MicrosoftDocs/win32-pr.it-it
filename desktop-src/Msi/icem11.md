---
description: ICEM11 verifica che in un modulo di merge configurabile sia elencata la tabella ModuleConfiguration e la tabella ModuleSubstitution nella tabella ModuleIgnoreTable del modulo.
ms.assetid: f0199137-0a40-40ca-b3cf-ff8eef4309cc
title: ICEM11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 157248d62f43a0b1a791220e2aeb917ba8273d31b93de69078f9876cddbd2748
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894431"
---
# <a name="icem11"></a>ICEM11

ICEM11 verifica che in un modulo di merge configurabile sia elencata la tabella [ModuleConfiguration](moduleconfiguration-table.md) e la tabella [ModuleSubstitution](modulesubstitution-table.md) nella [tabella ModuleIgnoreTable](moduleignoretable-table.md) del modulo. In questo modo, gli strumenti di unione che non riconoscono i moduli unione configurabili (versione 2.0) non copiano queste tabelle nel database di destinazione.

Questo icem è disponibile nel file Mergemod.cub disponibile in Windows Installer 2.0 SDK e versioni successive. Per informazioni dettagliate, vedere [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).

## <a name="result"></a>Risultato

ICEM11 invia un errore se il modulo contiene una tabella ModuleConfiguration o ModuleSubstitution non elencata nella tabella ModuleIgnoreTable.

## <a name="example"></a>Esempio

ICEM11 invia i messaggi di errore seguenti per un modulo contenente le voci di database illustrate di seguito.

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
| Control | Dialog1; Controllo1 | Testo   | \[IconKey1\] |



 

[ModuleIgnoreTable](moduleignoretable-table.md)



| Tabella               |
|---------------------|
| ModuleConfiguration |



 

Per correggere questo errore, includere entrambe le tabelle ModuleSubstitution e ModuleConfiguration nella tabella ModuleIgnoreTable.

## <a name="table-used-during-execution"></a>Tabella usata durante l'esecuzione

[ModuleSubstitution](modulesubstitution-table.md)

[ModuleConfiguration](moduleconfiguration-table.md)

[ModuleIgnoreTable](moduleignoretable-table.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento sul modulo di unione ICE](merge-module-ice-reference.md)
</dt> </dl>

 

 



