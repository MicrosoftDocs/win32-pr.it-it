---
description: La tabella Font contiene le informazioni per la registrazione dei file dei tipi di carattere con il sistema.
ms.assetid: 5ddff430-a6f8-473b-8006-ac0124469a99
title: Tabella dei tipi di carattere
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65efb786d4379bbe14fec0239cd8f3edee50f1b79a6413904b6e00331bc49a25
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118946982"
---
# <a name="font-table"></a>Tabella dei tipi di carattere

La tabella Font contiene le informazioni per la registrazione dei file dei tipi di carattere con il sistema.

Nella tabella Tipo di carattere sono disponibili le colonne seguenti.



| Colonna    | Tipo                         | Chiave | Nullable |
|-----------|------------------------------|-----|----------|
| file\_    | [Identificatore](identifier.md) | S   | N        |
| FontTitle | [Text](text.md)             | N   | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_
</dt> <dd>

Chiave esterna nella voce [della tabella File](file-table.md) per il file del tipo di carattere. È consigliabile che per il componente contenente il file del tipo di carattere sia specificato FontsFolder nella colonna Directory \_ della [tabella Component](component-table.md).

</dd> <dt>

<span id="FontTitle"></span><span id="fonttitle"></span><span id="FONTTITLE"></span>FontTitle
</dt> <dd>

Nome del tipo di carattere. È consigliabile lasciare null questa colonna per i tipi di carattere TrueType e le raccolte TrueType perché il programma di installazione può registrare il tipo di carattere dopo aver letto il titolo del tipo di carattere corretto dal file del tipo di carattere. Se viene immesso il nome del tipo di carattere, deve essere identico al titolo del tipo di carattere del file del tipo di carattere. È necessario specificare un titolo per i tipi di carattere che non hanno nomi incorporati, ad esempio file con estensione fon.

</dd> </dl>

## <a name="remarks"></a>Commenti

A questa tabella viene fatto riferimento quando viene eseguita [l'azione RegisterFonts](registerfonts-action.md) o [UnregisterFonts.](unregisterfonts-action.md)

Se il campo FontTitle viene lasciato Null, il nome del tipo di carattere viene letto direttamente dal file del tipo di carattere specificato. Se il nome del tipo di carattere registrato nel campo FontTitle è diverso da quello interno registrato nel file del tipo di carattere, il tipo di carattere viene registrato due volte dall'azione [RegisterFonts](registerfonts-action.md).

I file dei tipi di carattere non devono essere creati con un ID lingua, perché i tipi di carattere non dispongono di una risorsa ID lingua incorporata. Pertanto, la colonna Language della tabella [File deve](file-table.md) essere lasciata null per i file dei tipi di carattere.

Poiché il programma di installazione non fa riferimento ai file dei tipi di carattere per impostazione predefinita, i file dei tipi di carattere preesistenti possono essere rimossi con il relativo componente durante la disinstallazione di un'applicazione. Per assicurarsi che un file del tipo di carattere non venga rimosso, gli autori possono impostare i flag di bit **msidbComponentAttributesSharedDllRefCount** o **msidbComponentAttributesPermanent** nella colonna Attributi della tabella dei componenti msi Component Table per il componente che contiene il file del tipo di \_ \_ \_ carattere.

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE07](ice07.md)  
[ICE32](ice32.md)  
[ICE51](ice51.md)  
[ICE60](ice60.md)  
</dl>

 

 



