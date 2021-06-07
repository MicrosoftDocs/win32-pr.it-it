---
title: Modifiche al modello in modalità IME
description: Il modello in modalità IME è stato modificato da per utente a per thread
ms.assetid: C9717AF2-7055-47CA-8F8F-BC0F483B2259
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30404b1a386c4346e7d8900481d8c5198972cdbe
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443248"
---
# <a name="ime-mode-model-changed-from-per-user-to-per-thread"></a>Il modello in modalità IME è stato modificato da per utente a per thread

## <a name="platforms"></a>Piattaforme

<dl> Client - Windows 8.1  
Servers - Windows Server 2012 R2  
</dl>

## <a name="description"></a>Descrizione

In Windows 8, la modalità di conversione IME e la modalità frase IME si basavano sul contesto utente e la modifica della modalità di un'applicazione ha interessato tutte le altre applicazioni. Questo comportamento può essere disabilitato usando l'impostazione "Consenti di impostare un metodo di input diverso per ogni finestra dell'app" nella sezione impostazioni avanzate del pannello di controllo della lingua.

Per migliorare la compatibilità, in Windows 8.1 le modalità vengono archiviate in un contesto di input indipendentemente dalla modalità di impostazione del controllo "Consenti di impostare un metodo di input diverso per ogni finestra dell'app". In Windows 8.1 l'impostazione "Consenti di impostare un metodo di input diverso per ogni finestra dell'app" influisce solo sulla selezione del metodo di input stesso.

All'avvio dell'applicazione, la modalità IME è impostata sul valore predefinito seguente:



| &nbsp;   | Pannello di input software | Tastiera hardware |
|----------|----------------------|-------------------|
| KOR, JPN | Attivato                   | Disattivato               |
| CHS, CHT  | On                   | On                |



 

## <a name="manifestations"></a>Manifestazioni

Quando un utente modifica la modalità IME in un'applicazione, la modifica non influisce sulle altre applicazioni.

## <a name="resources"></a>Risorse

-   [Valori della modalità di conversione IME](../intl/ime-conversion-mode-values.md)
-   [Valori della modalità frase IME](../intl/ime-sentence-mode-values.md)

 

 