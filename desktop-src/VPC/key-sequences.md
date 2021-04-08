---
title: Sequenze di chiavi
description: Una stringa di sequenza di chiavi è un set delimitato da virgole di identificatori di chiave usati per simulare la sequenza di stampa e di rilascio della chiave di una tastiera standard in stile US 101-Key.
ms.assetid: 6f5301d1-af6e-4b43-8884-c76b2300ba92
keywords:
- Virtual PC virtuale Windows, sequenze di chiavi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b0c973b5aafd3bf02746ac1550ffedf3d4a4c1f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729282"
---
# <a name="key-sequences"></a>Sequenze di chiavi

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Una stringa di sequenza di chiavi è un set delimitato da virgole di identificatori di chiave usati per simulare la sequenza di stampa e di rilascio della chiave di una tastiera standard in stile US 101-Key.

Se un identificatore di chiave viene visualizzato nella stringa senza un modificatore precedente, viene simulato un codice con pressione chiave, seguito immediatamente dal codice corrispondente rilasciato dalla chiave. Per modificare questo comportamento, è possibile usare i modificatori di chiave.

Il modificatore **Down** , ad esempio, invierà il codice premuto per la chiave per l'identificatore di chiave seguente senza inviare il codice rilasciato dalla chiave. Questa operazione è utile per la simulazione dei tasti CTRL, ALT e MAIUSC quando vengono mantenuti mentre sono in corso l'invio di altri tasti. Per rilasciare la chiave, è necessario includerla nuovamente nella stringa della chiave insieme a un modificatore **up** precedente.

## <a name="key-identifiers"></a>Identificatori di chiave

Nell'elenco seguente vengono illustrate in dettaglio le stringhe valide dell'identificatore di chiave. 

| Stringa dell'identificatore di chiave | Significato                         |
|-----------------------|---------------------------------|
| Escape della chiave \_           | tasto **ESC**                 |
| Chiave \_ F1               | tasto **F1**                  |
| Chiave \_ F2               | tasto **F2**                  |
| Chiave \_ F3               | tasto **F3**                  |
| Chiave \_ F4               | tasto **F4**                  |
| Tasto \_ F5               | tasto **F5**                  |
| Chiave \_ F6               | tasto **F6**                  |
| Chiave \_ F7               | tasto **F7**                  |
| Chiave \_ F8               | tasto **F8**                  |
| Tasto \_ F9               | tasto **F9**                  |
| Chiave \_ F10              | tasto **F10**                 |
| Chiave \_ F11              | tasto **F11**                 |
| Chiave \_ F12              | tasto **F12**                 |
| \_SysReq chiave           | chiave **SysReq**              |
| \_ScrollLock chiave       | chiave **ScrollLock**          |
| Chiave \_ break            | tasto **INTERR**               |
| \_LeftApostrophe chiave   | **\`** chiave                  |
| Chiave \_ 1                | chiave **1**                   |
| Chiave \_ 2                | tasto **2**                   |
| Chiave \_ 3                | tasto **3**                   |
| Chiave \_ 4                | tasto **4**                   |
| Chiave \_ 5                | tasto **5**                   |
| Chiave \_ 6                | tasto **6**                   |
| Chiave \_ 7                | tasto **7**                   |
| Chiave \_ 8                | tasto **8**                   |
| Chiave \_ 9                | tasto **9**                   |
| Chiave \_ 0                | tasto **0**                   |
| \_Segno meno della chiave           | **-** chiave                   |
| Chiave \_ uguale a           | **=** chiave                   |
| BACKSPACE della chiave \_        | tasto **BACKSPACE**           |
| \_Inserimento chiave           | chiave **ins**                 |
| \_Home page chiave             | chiave **Home**                |
| \_PageUp chiave           | chiave **PageUp**              |
| \_NumLock chiave          | chiave **NumLock**             |
| \_Divisione tastiera        | **/** chiave del tastierino     |
| \_Moltiplicazione tastiera      | **\*** chiave del tastierino    |
| Tastierino \_ meno         | **-** chiave del tastierino     |
| \_Scheda chiave              | tasto **Tab**                 |
| Chiave \_ Q                | tasto **Q**                   |
| Chiave \_ W                | tasto **W**                   |
| Chiave \_ E                | chiave **E**                   |
| Chiave \_ R                | chiave **R**                   |
| Chiave \_ T                | tasto **T**                   |
| Chiave \_ Y                | il tasto **Y**                   |
| Chiave \_ U                | tasto **U**                   |
| Chiave \_ I                | chiave **i**                   |
| Chiave \_ O                | tasto **O**                   |
| Chiave \_ P                | tasto **P**                   |
| \_LeftBracket chiave      | **\[** chiave                  |
| \_RightBracket chiave     | **\]** chiave                  |
| \_Barra rovesciata chiave        | **\\** chiave                  |
| \_Elimina chiave           | tasto **Canc**              |
| \_Estremità chiave              | tasto **fine**                 |
| \_PGGIÙ chiave         | chiave **PGGIÙ**            |
| Tastierino \_ 7             | tasto **7** del tastierino     |
| Tastierino \_ 8             | tasto **8** sul tastierino     |
| Tastierino \_ 9             | tasto **9** del tastierino     |
| Tastierino \_ Plus          | **+** chiave del tastierino     |
| Chiave \_ A                | chiave **A**                   |
| Chiave \_ S                | tasto **S**                   |
| Chiave \_ D                | tasto **D**                   |
| Chiave \_ F                | tasto **F**                   |
| Chiave \_ G                | tasto **G**                   |
| Chiave \_ H                | tasto **H**                   |
| Chiave \_ J                | tasto **J**                   |
| Chiave \_ K                | tasto **K**                   |
| Chiave \_ L                | tasto **L**                   |
| \_Punto e virgola chiave        | chiave **.**                   |
| \_SINGLEQUOTE chiave      | chiave                    |
| \_Immissione chiave            | tasto **invio**               |
| Tastierino \_ 4             | tasto **4** sul tastierino     |
| Tastierino \_ 5             | tasto **5** del tastierino     |
| Tastierino \_ 6             | tasto **6** del tastierino     |
| \_LeftShift chiave        | tasto **MAIUSC sinistro**          |
| Chiave \_ Z                | tasto **Z**                   |
| Chiave \_ X                | tasto **X**                   |
| Chiave \_ C                | chiave **C**                   |
| Chiave \_ V                | tasto **V**                   |
| Chiave \_ B                | chiave **B**                   |
| Chiave \_ N                | tasto **N**                   |
| Chiave \_ M                | tasto **M**                   |
| \_Virgola chiave            | **,** chiave                   |
| \_Periodo chiave           | oggetto **.** key                   |
| Barra della chiave \_            | **/** chiave                   |
| \_RightShift chiave       | tasto **MAIUSC destro**         |
| Chiave \_ su               | tasto **up**                  |
| Tastierino \_ 1             | tasto **1** sul tastierino     |
| Tastierino \_ 2             | tasto **2** sul tastierino     |
| Tastierino \_ 3             | tasto **3** del tastierino     |
| \_INVIO tastiera         | tasto **invio** sul tastierino |
| \_LeftCtrl chiave         | tasto **CTRL sinistro**           |
| \_LeftWindows chiave      | tasto **Windows sinistro**        |
| \_LeftAlt chiave          | tasto **ALT sinistro**            |
| \_Spazio chiave            | chiave **dello spazio**               |
| \_AltDestro chiave         | tasto **ALT destro**           |
| \_RightWindows chiave     | tasto **Windows destro**       |
| \_RightCtrl chiave        | tasto **CTRL destro**          |
| \_Applicazione chiave      | chiave **dell'applicazione**         |
| Chiave a \_ sinistra             | tasto **sinistro**                |
| Tasto \_ giù             | tasto **giù**                |
| Chiave a \_ destra            | tasto **destro**               |
| Tastierino \_ 0             | tasto **0** sul tastierino     |
| Tastiera \_ DecimalPoint  | oggetto **.** chiave del tastierino     |



 

## <a name="key-modifiers"></a>Modificatori di chiave

Nell'elenco seguente vengono illustrate in dettaglio le stringhe del modificatore di chiave valide. 

| Stringa modificatore chiave | Significato                                                                                       |
|---------------------|-----------------------------------------------------------------------------------------------|
| DOWN                | Inviare un codice premuto con la chiave per l'identificatore di chiave seguente senza inviare un codice rilasciato dalla chiave. |
| UP                  | Inviare un codice rilasciato dalla chiave per l'identificatore di chiave seguente.                                    |
| HOLD                | Sospendere 200 millisecondi prima di continuare a elaborare il resto della stringa della sequenza di chiavi. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IVMKeyboard**](ivmkeyboard.md)
</dt> </dl>

 

 