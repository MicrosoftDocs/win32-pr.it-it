---
title: Modifiche al modello in modalità IME
description: Modello in modalità IME modificato da per utente a per thread
ms.assetid: C9717AF2-7055-47CA-8F8F-BC0F483B2259
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 781c322949f17d4d3313b6a9b7b5eff9b1e83b06
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338838"
---
# <a name="ime-mode-model-changed-from-per-user-to-per-thread"></a>Modello in modalità IME modificato da per utente a per thread

## <a name="platforms"></a>Piattaforme

<dl> Client-Windows 8.1  
Server-Windows Server 2012 R2  
</dl>

## <a name="description"></a>Descrizione

In Windows 8, la modalità di conversione IME e la modalità frase IME sono basate sul contesto utente e la modifica della modalità di un'applicazione ha interessato tutte le altre applicazioni. Questo comportamento può essere disabilitato usando l'impostazione "Consenti impostazione di un metodo di input diverso per ogni finestra dell'app" nella sezione Impostazioni avanzate del pannello di controllo della lingua.

Per migliorare la compatibilità, in Windows 8.1 le modalità vengono archiviate in un contesto di input indipendentemente dalla modalità di impostazione del controllo "Consenti impostazione di un metodo di input diverso per ogni finestra dell'app". In Windows 8.1 l'impostazione "Consenti impostazione di un metodo di input diverso per ogni finestra dell'app" influiscono solo sulla selezione del metodo di input.

All'avvio dell'applicazione, la modalità IME è impostata sui valori predefiniti seguenti:



|          | Pannello di input software | Tastiera hardware |
|----------|----------------------|-------------------|
| KOR, JPN | Attivato                   | Disattivato               |
| CHS, CHT  | Attivato                   | Attivato                |



 

## <a name="manifestations"></a>Manifestazioni

Quando un utente modifica la modalità IME in un'applicazione, la modifica non influisce sulle altre applicazioni.

## <a name="resources"></a>Risorse

-   [Valori della modalità di conversione IME](../intl/ime-conversion-mode-values.md)
-   [Valori della modalità frase IME](../intl/ime-sentence-mode-values.md)

 

 