---
title: Sequenze di chiavi
description: Una stringa di sequenza di tasti è un set delimitato da virgole di identificatori di tasto che vengono usati per simulare la sequenza di pressione e rilascio di una tastiera AT standard degli Stati Uniti a 101 tasti.
ms.assetid: 6f5301d1-af6e-4b43-8884-c76b2300ba92
keywords:
- Windows Virtual PC Virtual PC , sequenze di chiavi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b300c1d417bad30f7a0e06fd8cfb411184eb8f6b800549536c9b6452dcdfefa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118591446"
---
# <a name="key-sequences"></a>Sequenze di chiavi

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Una stringa di sequenza di tasti è un set delimitato da virgole di identificatori di tasto che vengono usati per simulare la sequenza di pressione e rilascio di una tastiera AT standard degli Stati Uniti a 101 tasti.

Se nella stringa viene visualizzato un identificatore di tasto senza un modificatore precedente, viene simulato un codice premuto tramite tasto, seguito immediatamente dal codice corrispondente rilasciato dal tasto. I modificatori di tasto possono essere usati per modificare questo comportamento.

Ad esempio, il **modificatore DOWN** invierà il codice premuto per il tasto seguente senza inviare il codice rilasciato dal tasto. Ciò è utile per simulare i tasti CTRL, ALT e MAIUSC quando vengono premuti mentre vengono inviati altri tasti. Per rilasciare il tasto, è necessario includerlo di nuovo nella stringa chiave insieme a un modificatore **UP** precedente.

## <a name="key-identifiers"></a>Identificatori di chiave

Nell'elenco seguente vengono fornite informazioni dettagliate sulle stringhe di identificatori di chiave valide. 

| Stringa dell'identificatore di chiave | Significato                         |
|-----------------------|---------------------------------|
| Key \_ Escape           | tasto **ESC**                 |
| Tasto \_ F1               | tasto **F1**                  |
| Tasto \_ F2               | tasto **F2**                  |
| Tasto \_ F3               | tasto **F3**                  |
| Tasto \_ F4               | tasto **F4**                  |
| Tasto \_ F5               | tasto **F5**                  |
| Tasto \_ F6               | tasto **F6**                  |
| Tasto \_ F7               | tasto **F7**                  |
| Tasto \_ F8               | tasto **F8**                  |
| Tasto \_ F9               | tasto **F9**                  |
| Tasto \_ F10              | tasto **F10**                 |
| Tasto \_ F11              | tasto **F11**                 |
| Tasto \_ F12              | tasto **F12**                 |
| \_SysReq chiave           | la **chiave SysReq**              |
| Tasto \_ ScrollLock       | Tasto **ScrollLock**          |
| Interruzione \_ di tasto            | Tasto **Interrompi**               |
| Key \_ LeftApostrophe   | la **\`** chiave                  |
| Chiave \_ 1                | tasto **1**                   |
| Chiave \_ 2                | tasto **2**                   |
| Chiave \_ 3                | tasto **3**                   |
| Chiave \_ 4                | tasto **4**                   |
| Chiave \_ 5                | tasto **5**                   |
| Chiave \_ 6                | tasto **6**                   |
| Chiave \_ 7                | tasto **7**                   |
| Chiave \_ 8                | tasto **8**                   |
| Chiave \_ 9                | tasto **9**                   |
| Chiave \_ 0                | tasto **0**                   |
| Trattino \_ chiave           | la **-** chiave                   |
| Chiave \_ uguale a           | la **=** chiave                   |
| Backspace \_ chiave        | tasto **BACKSPACE**           |
| Inserimento \_ chiave           | Tasto **Ins**                 |
| Home \_ page chiave             | Tasto **Home**                |
| Key \_ PageUp           | Tasto **PTTAP**              |
| Tasto \_ NumLock          | tasto **NumLock**             |
| Divisione del \_ tastierino        | tasto **/** sul tastierino     |
| Moltiplicazione del \_ tastierino      | tasto **\*** sul tastierino    |
| Tastierino \_ meno         | tasto **-** sul tastierino     |
| Tasto \_ TAB              | tasto **TAB**                 |
| Chiave \_ Q                | tasto **Q**                   |
| Chiave \_ W                | tasto **W**                   |
| Chiave \_ E                | tasto **E**                   |
| Chiave \_ R                | tasto **R**                   |
| Chiave \_ T                | tasto **T**                   |
| Chiave \_ Y                | tasto **Y**                   |
| Tasto \_ U                | tasto **U**                   |
| Chiave \_ I                | tasto **I**                   |
| Chiave \_ O                | tasto **O**                   |
| Chiave \_ P                | tasto **P**                   |
| Key \_ LeftBracket      | chiave **\[**                  |
| Key \_ RightBracket     | chiave **\]**                  |
| Barra \_ rovesciata della chiave        | chiave **\\**                  |
| Eliminazione \_ della chiave           | tasto  CANC              |
| Fine \_ chiave              | tasto  fine                 |
| PageDown \_ chiave         | tasto **PageDown**            |
| Tastiera \_ 7             | tasto **7** sul tastierino     |
| Tastiera \_ 8             | tasto **8** sul tastierino     |
| Tastiera \_ 9             | tasto **9** sul tastierino     |
| Tastierino \_ più          | tasto **+** sulla tastiera     |
| Chiave \_ A                | la **chiave A**                   |
| Chiave \_ S                | tasto **S**                   |
| Chiave \_ D                | chiave **D**                   |
| Tasto \_ F                | tasto **F**                   |
| Tasto \_ G                | tasto **G**                   |
| Chiave \_ H                | tasto **H**                   |
| Chiave \_ J                | tasto **J**                   |
| Chiave \_ K                | tasto **K**                   |
| Chiave \_ L                | tasto **L**                   |
| Punto \_ e virgola chiave        | la **chiave ;**                   |
| Chiave \_ SingleQuote      | la **chiave '**                   |
| Tasto \_ INVIO            | tasto  INVIO               |
| Tastiera \_ 4             | tasto **4** sul tastierino     |
| Tastiera \_ 5             | **5** tasti sul tastierino     |
| Tastiera \_ 6             | tasto **6** sul tastierino     |
| Key \_ LeftShift        | tasto **MAIUSC sinistro**          |
| Tasto \_ Z                | tasto **Z**                   |
| Chiave \_ X                | tasto **X**                   |
| Chiave \_ C                | tasto **C**                   |
| Chiave \_ V                | tasto **V**                   |
| Chiave \_ B                | tasto **B**                   |
| Chiave \_ N                | tasto **N**                   |
| Chiave \_ M                | tasto **M**                   |
| Virgola \_ chiave            | la **chiave ,**                   |
| Periodo \_ chiave           | oggetto **.** Key                   |
| Barra \_ della chiave            | chiave **/**                   |
| Tasto \_ DestroShift       | tasto **MAIUSC di** destra         |
| Key \_ Up               | Tasto **Su**                  |
| Tastiera \_ 1             | tasto **1** sul tastierino     |
| Tastiera \_ 2             | tasto **2** sul tastierino     |
| Tastiera \_ 3             | tasto **3** sul tastierino     |
| Invio del \_ tastierino numerico         | tasto **INVIO** sul tastierino numerico |
| Key \_ LeftCtrl         | tasto **CTRL SINISTRO**           |
| Tasto \_ SinistroWindows      | tasto **di scelta Windows** sinistra        |
| Chiave \_ LeftAlt          | tasto **ALT di** sinistra            |
| Spazio \_ delle chiavi            | tasto **SPAZIO**               |
| Chiave \_ RightAlt         | tasto **ALT di** destra           |
| Tasto \_ DestroWindows     | tasto **di scelta Windows** destra       |
| Key \_ RightCtrl        | tasto **CTRL** DESTRO          |
| Applicazione \_ chiave      | chiave **dell'applicazione**         |
| Tasto \_ sinistro             | tasto **SINISTRO**                |
| Tasto \_ GIÙ             | tasto **GIÙ**                |
| Tasto \_ destro            | tasto  destro               |
| Tastiera \_ 0             | tasto **0** sul tastierino     |
| Separatore \_ decimale del tastierino numerico  | oggetto **.** tasto sulla tastiera     |



 

## <a name="key-modifiers"></a>Modificatori di tasti

L'elenco seguente elenca in dettaglio le stringhe di modificatori di tasti valide. 

| Stringa del modificatore di chiave | Significato                                                                                       |
|---------------------|-----------------------------------------------------------------------------------------------|
| DOWN                | Inviare un codice premuto con il tasto per l'identificatore di tasto seguente senza inviare un codice rilasciato dal tasto. |
| UP                  | Inviare un codice rilasciato dalla chiave per l'identificatore di chiave seguente.                                    |
| HOLD                | Sospendere 200 millisecondi prima di continuare a elaborare il resto della stringa della sequenza di chiavi. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IVMKeyboard**](ivmkeyboard.md)
</dt> </dl>

 

 