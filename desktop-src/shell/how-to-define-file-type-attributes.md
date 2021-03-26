---
description: Definizione degli attributi dei tipi di file nel registro di sistema.
ms.assetid: EE35E3E7-0573-45CA-A21A-89E50B86487D
title: Come definire gli attributi del tipo di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7844c65191d6513a06625a28c47accd3df5cc82f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881574"
---
# <a name="how-to-define-file-type-attributes"></a>Come definire gli attributi del tipo di file

L'assegnazione di attributi di tipo file a un ProgID associato consente di controllare alcuni aspetti del comportamento del tipo di file. Prima di Windows Vista, questi attributi potevano consentire di limitare la portata a cui l'utente può utilizzare la scheda delle proprietà **Opzioni cartella** per modificare diversi aspetti del tipo di file, ad esempio l'icona o i verbi.

Gli attributi del tipo di file sono flag binari specificati come **reg \_ DWORD** o valori **\_ binari reg** nella sottochiave ProgID associata al tipo di file.

Per assegnare attributi per un tipo di file, attenersi alla seguente procedura.

## <a name="instructions"></a>Istruzioni

### <a name="step-1"></a>Passaggio 1:

Aggiungere una voce flag alla sottochiave ProgID associata al tipo di file.

### <a name="step-2"></a>Passaggio 2:

Impostare la voce sul valore dell'attributo appropriato.

Nell'esempio seguente vengono illustrati gli \_ attributi di FTA NoRemove (0x00000010) e FTA \_ NoNewVerb (0x00000020) impostati per il tipo di file con estensione MYP.

```
HKEY_CLASSES_ROOT
   .myp-file
      (Default) = ApplicationVendor.MyProgram
   ApplicationVendor.MyProgram
      (Default) = MyProgram Application
      EditFlags = 0x00000030
```

## <a name="remarks"></a>Commenti

I flag possono essere combinati con un OR logico per formare il singolo valore dell'attributo.

Per un elenco di possibili attributi dei tipi di file e dei relativi valori esadecimali e altri dettagli su come recuperare e impostare a livello di codice questi valori, vedere [**FILETYPEATTRIBUTEFLAGS**](/windows/desktop/api/Shlwapi/ne-shlwapi-filetypeattributeflags).

 

 



