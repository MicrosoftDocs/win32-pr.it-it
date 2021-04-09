---
description: La tabella font contiene le informazioni per la registrazione dei file del tipo di carattere con il sistema.
ms.assetid: 5ddff430-a6f8-473b-8006-ac0124469a99
title: Tabella dei tipi di carattere
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c10208c7b9a14ca7f311aff71653a53a3da9ed0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967807"
---
# <a name="font-table"></a>Tabella dei tipi di carattere

La tabella font contiene le informazioni per la registrazione dei file del tipo di carattere con il sistema.

La tabella font contiene le colonne seguenti.



| Colonna    | Tipo                         | Chiave | Nullable |
|-----------|------------------------------|-----|----------|
| file\_    | [Identificatore](identifier.md) | S   | N        |
| FontTitle | [Text](text.md)             | N   | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_
</dt> <dd>

Chiave esterna nella voce della [tabella file](file-table.md) per il file del tipo di carattere. È consigliabile che il componente contenente il file del tipo di carattere includa il FontsFolder specificato nella \_ colonna directory della [tabella dei componenti](component-table.md).

</dd> <dt>

<span id="FontTitle"></span><span id="fonttitle"></span><span id="FONTTITLE"></span>FontTitle
</dt> <dd>

Nome del tipo di carattere. Si consiglia di lasciare questa colonna null per i tipi di carattere TrueType e le raccolte TrueType perché il programma di installazione può registrare il tipo di carattere dopo la lettura del titolo del tipo di carattere corretto dal file del tipo di carattere. Se il nome del tipo di carattere viene immesso, deve essere identico al titolo del carattere dal file del tipo di carattere. È necessario specificare un titolo per i tipi di carattere che non hanno nomi incorporati, ad esempio i file con estensione fon.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa tabella viene definita quando viene eseguita l'azione [RegisterFonts](registerfonts-action.md) o [UnregisterFonts](unregisterfonts-action.md) .

Se il campo FontTitle viene lasciato null, il nome del tipo di carattere viene letto direttamente dal file del tipo di carattere specificato. Se il nome del tipo di carattere registrato nel campo FontTitle è diverso dal nome del tipo di carattere interno registrato nel file del tipo di carattere, il tipo di carattere viene registrato due volte dall' [azione RegisterFonts](registerfonts-action.md).

I file del tipo di carattere non devono essere creati con un ID lingua, perché i tipi di carattere non hanno una risorsa ID lingua incorporata. In questo modo, la colonna lingua della [tabella file](file-table.md) deve essere lasciata null per i file del tipo di carattere.

Poiché il programma di installazione non refcount i file del tipo di carattere per impostazione predefinita, i file dei tipi di carattere preesistenti possono essere rimossi con il componente durante la disinstallazione di un'applicazione. Per assicurarsi che un file del tipo di carattere non venga rimosso, gli autori possono impostare i flag di bit **msidbComponentAttributesSharedDllRefCount** o **MsidbComponentAttributesPermanent** nella colonna attributi della tabella dei componenti MSI della tabella dei componenti \_ \_ \_ per il componente contenente il file del tipo di carattere.

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE07](ice07.md)  
[ICE32](ice32.md)  
[ICE51](ice51.md)  
[ICE60](ice60.md)  
</dl>

 

 



