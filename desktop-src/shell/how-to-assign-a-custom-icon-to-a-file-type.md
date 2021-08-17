---
description: Un'icona personalizzata deve essere assegnata a un tipo di file per fornire un'indicazione visiva all'utente di tale tipo di file o all'applicazione a cui è associato il tipo di file.
ms.assetid: 84F293C2-BAB1-4BF8-9F89-122B6DAB29C3
title: Come assegnare un'icona personalizzata a un tipo di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d156322bfe0899ed48c6c27f2660b911d9e5c77791c550b6141144d95384b6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092997"
---
# <a name="how-to-assign-a-custom-icon-to-a-file-type"></a>Come assegnare un'icona personalizzata a un tipo di file

Quando a un tipo di file non viene assegnata alcuna icona predefinita personalizzata, il desktop e Windows Explorer visualizzano tutti i file di quel tipo con un'icona predefinita generica. Ad esempio, la schermata seguente mostra questa icona predefinita usata con il file MyDocs4.myp.

![Screenshot dell'icona predefinita](images/icon.png)

Mentre tutti i file visualizzati in questa schermata sono semplici file di testo, solo MyDocs4.myp visualizza l'icona Windows predefinita. Questo perché l'.txt è un tipo di file registrato con un'icona predefinita personalizzata.

La schermata seguente mostra un'icona personalizzata assegnata al tipo di file con estensione myp.

![Screenshot dell'icona personalizzata per i file con estensione myp](images/context4.png)

> [!Note]  
> Le icone possono anche essere assegnate in base a un'applicazione specifica.

 

## <a name="instructions"></a>Istruzioni

### <a name="step-1"></a>Passaggio 1:

Creare una sottochiave **denominata DefaultIcon** in una delle due posizioni seguenti:

-   Per un'assegnazione di tipo file, **HKEY \_ CLASSES \_ ROOT** \\ *.extension*
-   Per un'assegnazione di applicazione, **HKEY \_ CLASSES \_ ROOT** \\ *ProgID*

### <a name="step-2"></a>Passaggio 2:

Assegnare **alla sottochiave DefaultIcon** un valore predefinito di tipo **REG \_ SZ** che specifica il percorso completo del file che contiene l'icona.

### <a name="step-3"></a>Passaggio 3:

Chiamare la [**funzione SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) per notificare a Shell di aggiornare la cache delle icone.

## <a name="remarks"></a>Commenti

Nell'esempio seguente viene illustrata una visualizzazione dettagliata delle voci del Registro di sistema necessarie per l'assegnazione di un'icona di tipo file. L'estensione di file è associata a un'applicazione, ma l'assegnazione dell'icona è all'estensione di file stessa in modo che l'applicazione associata non imposi l'icona predefinita.

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
      DefaultIcon
         (Default) = C:\MyDir\MyProgram.exe,2
```

Nell'esempio seguente viene illustrata una visualizzazione dettagliata delle voci del Registro di sistema necessarie per l'assegnazione di un'icona dell'applicazione. L'estensione myp viene prima associata all'applicazione MyProgram.1. Alla sottochiave MyProgram.1 ProgID viene quindi assegnata l'icona predefinita personalizzata.

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   MyProgram.1
      DefaultIcon
         (Default) = C:\MyDir\MyProgram.exe,2
```

Qualsiasi file che contiene un'icona è accettabile, inclusi i file con estensione ico, .exe e .dll file. Se nel file è presente più di un'icona, il percorso deve essere seguito da una virgola e quindi dall'indice dell'icona.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di file](fa-file-types.md)
</dt> </dl>

 

 



