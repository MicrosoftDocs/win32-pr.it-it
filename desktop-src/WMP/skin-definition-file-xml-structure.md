---
title: Struttura XML del file di definizione dell'interfaccia
description: Struttura XML del file di definizione dell'interfaccia
ms.assetid: 93325b94-667a-42a6-92f8-78288d36da81
keywords:
- creazione di interfaccia, file di definizione dell'interfaccia
- Windows Media Player, file di definizione dell'interfaccia
- skins, file di definizione dell'interfaccia
- file per le interfaccia, definizione dell'interfaccia
- file di definizione dell'interfaccia, struttura XML
- Struttura XML per i file di definizione dell'interfaccia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbc3506ab03d3af7445e75983299577c713412fbeb0899d39c7098c55be2450a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995251"
---
# <a name="skin-definition-file-xml-structure"></a>Struttura XML del file di definizione dell'interfaccia

Il file di definizione dell'interfaccia è scritto in XML. Una delle funzionalità importanti di XML è che è completamente strutturato ed è simile a una struttura. Il codice XML è semplicemente una serie di elementi, ad **esempio VIEW** e **BUTTONGROUP.** Si inizierà con gli elementi e quindi li si definirà con attributi. Nella parte restante di questa esercitazione verranno fornite informazioni dettagliate sugli attributi, ma di seguito è illustrata la struttura degli elementi che verranno usati:


```C++
<THEME>
    <VIEW>
        <BUTTONGROUP>
            <BUTTONELEMENT/>
            <BUTTONELEMENT/>
        </BUTTONGROUP>
    </VIEW>
<THEME>

```



Tenendo presente la semplice struttura degli elementi, è possibile dare un senso agli attributi che rendono univoco ogni elemento. I dettagli di ogni elemento verranno trattati negli argomenti rimanenti di questa sezione. Per altre informazioni su elementi e attributi, vedere Le informazioni [di riferimento sulla programmazione dell'interfaccia](skin-programming-reference.md)utente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Creazione del file di definizione dell'interfaccia**](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




