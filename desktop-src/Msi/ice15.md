---
description: ICE15 verifica che i riferimenti al tipo di contenuto e all'estensione nelle tabelle MIME ed Extension siano reciproci. La tabella MIME deve fare riferimento a un tipo di contenuto a un'estensione a cui la tabella extension fa riferimento allo stesso tipo di contenuto.
ms.assetid: 8a38c8d2-324d-4de9-932b-d188ff5ccbaf
title: ICE15
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ce1e5e54dedd2663a9f849abee43e244c73d7aa5835426be05d4e0163f599ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119529311"
---
# <a name="ice15"></a>ICE15

ICE15 verifica che i riferimenti al tipo di contenuto e all'estensione [nelle tabelle MIME](mime-table.md) ed [Extension](extension-table.md) siano reciproci. La tabella MIME deve fare riferimento a un tipo di contenuto a un'estensione a cui la tabella extension fa riferimento allo stesso tipo di contenuto.

Più estensioni possono fare riferimento allo stesso tipo MIME, purché il tipo MIME faccia riferimento a una delle estensioni. Più tipi MIME possono fare riferimento alla stessa estensione, purché l'estensione faccia riferimento a uno dei tipi MIME.

Si noti che ogni volta che un mime fa riferimento a un'estensione, tale estensione non può avere la colonna MIME \_ nella tabella Extension impostata su Null.

## <a name="result"></a>Risultato

ICE15 invia un errore se i riferimenti al tipo di contenuto e all'estensione non sono reciproci.

## <a name="example"></a>Esempio

ICE15 pubblica due messaggi di errore per l'esempio illustrato:

-   Il tipo di contenuto test/x-flaps nella tabella MIME fa riferimento all'estensione tst, ma l'estensione tst nella tabella Extension fa riferimento a flaps/x-flaps. Questo non è reciproco.
-   Il tipo di contenuto flaps/x-flaps fa riferimento all'estensione flp, ma tale estensione ha una voce Null nella colonna MIME \_ della tabella Extension.

[Tabella MIME](mime-table.md) (parziale)



| ContentType   | Estensione\_ |
|---------------|-------------|
| test/x-test   | Tst         |
| flaps/x-flaps | Flp         |



 

[Tabella delle estensioni](extension-table.md) (parziale)



| Estensione | MIME\_        |
|-----------|---------------|
| Tst       | flaps/x-flaps |
| Flp       | Null          |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su ICE](ice-reference.md)
</dt> </dl>

 

 



