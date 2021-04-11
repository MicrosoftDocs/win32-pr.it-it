---
description: ICE51 verifica che sia stato fornito un titolo per i file di risorse del tipo di carattere.
ms.assetid: 5a57ba6e-d1fe-44ab-b72d-52b1f212c322
title: ICE51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38082d754564eead6d60a62e3b4cdcf9b1f0f94f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232857"
---
# <a name="ice51"></a>ICE51

ICE51 verifica che sia stato fornito un titolo per i file di risorse del tipo di carattere.

È necessario specificare un titolo per una risorsa del tipo di carattere senza nome incorporato. Solo i file di risorse del tipo di carattere. TTC,. ttf e. otf non richiedono un titolo, perché questi file contengono un nome incorporato. Non specificare un titolo per una risorsa del tipo di carattere contenente un nome incorporato, perché il tipo di carattere viene registrato due volte dal sistema.

**[Windows Installer 4,5 e versioni precedenti](not-supported-in-windows-installer-4-5.md):** ICE51 non controlla i file di risorse del tipo di carattere. otf.

## <a name="result"></a>Risultato

ICE51 Invia un errore se sono presenti file di risorse del tipo. TTC,. ttf e. otf con titoli. ICE51 pubblica un avviso se sono presenti altri file di risorse del tipo di carattere senza titolo.

## <a name="example"></a>Esempio

ICE51 segnala l'avviso seguente per l'esempio illustrato.

``` syntax
Font 'Font1' is a TTC\TTF\OTF font, but also has a title.
```

ICE51 segnala il seguente messaggio di errore per l'esempio illustrato.

``` syntax
Font 'Font2' does not have a title. Only TTC\TTF\OTF fonts do not need titles.
```

[Tabella file](file-table.md) (parziale)



| File  | FileName  |
|-------|-----------|
| Font1 | font1. ttf |
| Font2 | font2. fon |



 

[Tabella dei tipi di carattere](font-table.md)



| file\_ | FontTitle          |
|--------|--------------------|
| Font1  | Un tipo di carattere molto interessante |
| Font2  |                    |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> </dl>

 

 



