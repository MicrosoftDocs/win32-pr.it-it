---
description: ICE51 verifica che sia stato fornito un titolo per i file di risorse del tipo di carattere.
ms.assetid: 5a57ba6e-d1fe-44ab-b72d-52b1f212c322
title: ICE51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1187ad79aa23ca26ade28ecf92e6cde60beb9c8cc56540bec85f2ab1ae467f2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119763891"
---
# <a name="ice51"></a>ICE51

ICE51 verifica che sia stato fornito un titolo per i file di risorse del tipo di carattere.

È necessario specificare un titolo per una risorsa del tipo di carattere che non dispone di un nome incorporato. Solo i file di risorse del tipo di carattere .ttc, .ttf e .otf non richiedono un titolo, perché questi file contengono un nome incorporato. Non specificare un titolo per una risorsa del tipo di carattere che contiene un nome incorporato perché il sistema registra quindi il tipo di carattere due volte.

**[Windows Installer 4.5 e versioni precedenti:](not-supported-in-windows-installer-4-5.md)** ICE51 non controlla i file di risorse del tipo di carattere OTF.

## <a name="result"></a>Risultato

ICE51 invia un errore se sono presenti file di risorse con estensione ttc, ttf e otf con titoli. ICE51 invia un avviso se sono presenti altri file di risorse del tipo di carattere senza titolo.

## <a name="example"></a>Esempio

ICE51 segnalerebbe l'avviso seguente per l'esempio illustrato.

``` syntax
Font 'Font1' is a TTC\TTF\OTF font, but also has a title.
```

ICE51 segnala il messaggio di errore seguente per l'esempio illustrato.

``` syntax
Font 'Font2' does not have a title. Only TTC\TTF\OTF fonts do not need titles.
```

[Tabella file](file-table.md) (parziale)



| File  | FileName  |
|-------|-----------|
| Carattere1 | font1.ttf |
| Carattere2 | font2.fon |



 

[Tabella dei tipi di carattere](font-table.md)



| file\_ | CarattereTitle          |
|--------|--------------------|
| Carattere1  | Un tipo di carattere davvero interessante |
| Carattere2  |                    |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su ICE](ice-reference.md)
</dt> </dl>

 

 



