---
description: Definizione degli attributi del tipo di file nel Registro di sistema.
ms.assetid: EE35E3E7-0573-45CA-A21A-89E50B86487D
title: Come definire gli attributi dei tipi di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e0a89f5770b55521ccdf51859bdde69ed58d05f864385e46f1d76e482319c63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118223575"
---
# <a name="how-to-define-file-type-attributes"></a>Come definire gli attributi dei tipi di file

L'assegnazione di attributi del tipo di file a un ProgID associato consente di controllare alcuni aspetti del comportamento del tipo di file. Prima di Windows Vista, questi attributi potevano consentire di limitare la misura  in cui l'utente poteva usare la scheda delle proprietà Opzioni cartella per modificare vari aspetti del tipo di file, ad esempio l'icona o i verbi.

Gli attributi del tipo di file sono flag binari specificati come **\_ valori REG DWORD** o **REG \_ BINARY** nella sottochiave ProgID associata del tipo di file.

Per assegnare attributi per un tipo di file, seguire questa procedura.

## <a name="instructions"></a>Istruzioni

### <a name="step-1"></a>Passaggio 1:

Aggiungere una voce EditFlags alla sottochiave ProgID associata del tipo di file.

### <a name="step-2"></a>Passaggio 2:

Impostare la voce sul valore dell'attributo appropriato.

L'esempio seguente mostra gli attributi FTA \_ NoRemove (0x00000010) e FTA NoNewVerb (0x00000020) impostati per il tipo \_ di file myp.

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

Per un elenco dei possibili attributi del tipo di file e dei relativi valori esadecimali e per altri dettagli sul recupero e l'impostazione di questi valori a livello di codice, vedere [**FILETYPEATTRIBUTEFLAGS.**](/windows/desktop/api/Shlwapi/ne-shlwapi-filetypeattributeflags)

 

 



