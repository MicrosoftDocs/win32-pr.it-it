---
description: ICE15 verifica che il tipo di contenuto e i riferimenti all'estensione nelle tabelle MIME e Extension siano reciproci. La tabella MIME deve fare riferimento a un tipo di contenuto a un'estensione che la tabella di estensione fa riferimento allo stesso tipo di contenuto.
ms.assetid: 8a38c8d2-324d-4de9-932b-d188ff5ccbaf
title: ICE15
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb39b3c617db41e9e58a226f1eeb92c3d733ebad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104057811"
---
# <a name="ice15"></a>ICE15

ICE15 verifica che il tipo di contenuto e i riferimenti all'estensione nelle tabelle [MIME](mime-table.md) e [Extension](extension-table.md) siano reciproci. La tabella MIME deve fare riferimento a un tipo di contenuto a un'estensione che la tabella di estensione fa riferimento allo stesso tipo di contenuto.

Più estensioni possono fare riferimento allo stesso tipo MIME, purché il tipo MIME faccia riferimento a una delle estensioni. Più tipi MIME possono fare riferimento alla stessa estensione, purché l'estensione faccia riferimento a uno dei tipi MIME.

Si noti che ogni volta che un MIME fa riferimento a un'estensione, tale estensione non può avere la colonna MIME della \_ tabella di estensione impostata su null.

## <a name="result"></a>Risultato

ICE15 Invia un errore se il tipo di contenuto e i riferimenti all'estensione non sono reciproci.

## <a name="example"></a>Esempio

ICE15 invia due messaggi di errore per l'esempio illustrato:

-   Il tipo di contenuto test/x-flaps nella tabella MIME fa riferimento alla TST dell'estensione, ma il TST di estensione nella tabella di estensione fa riferimento a flap/x-flaps. Questo non è reciproco.
-   Il tipo di contenuto flaps/x-flaps fa riferimento all'estensione FLP, ma tale estensione include una voce null nella \_ colonna MIME della tabella di estensione.

[Tabella MIME](mime-table.md) (parziale)



| ContentType   | Estensione\_ |
|---------------|-------------|
| test/x-test   | TST         |
| Flap/x-flap | FLP         |



 

[Tabella di estensione](extension-table.md) (parziale)



| Estensione | MIME\_        |
|-----------|---------------|
| TST       | Flap/x-flap |
| FLP       | Null          |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> </dl>

 

 



