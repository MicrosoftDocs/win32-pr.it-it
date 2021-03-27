---
description: Un'icona personalizzata deve essere assegnata a un tipo di file per fornire un'indicazione visiva all'utente di quel tipo di file o all'applicazione a cui è associato il tipo di file.
ms.assetid: 84F293C2-BAB1-4BF8-9F89-122B6DAB29C3
title: Come assegnare un'icona personalizzata a un tipo di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf625eb6177471702096f462846b8035772177ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979618"
---
# <a name="how-to-assign-a-custom-icon-to-a-file-type"></a>Come assegnare un'icona personalizzata a un tipo di file

Quando nessuna icona personalizzata predefinita viene assegnata a un tipo di file, il desktop e Windows Explorer visualizzano tutti i file di quel tipo con un'icona generica predefinita. Ad esempio, lo screenshot seguente Mostra questa icona predefinita usata con il file MyDocs4. MYP.

![screenshot dell'icona predefinita](images/icon.png)

Mentre tutti i file visualizzati in questa schermata sono semplici file di testo, solo MyDocs4. MYP Visualizza l'icona predefinita di Windows. Questo è dovuto al fatto che l'estensione txt è un tipo di file registrato con un'icona predefinita personalizzata.

Lo screenshot seguente mostra un'icona personalizzata che è stata assegnata al tipo di file. MYP.

![screenshot dell'icona personalizzata per i file con estensione MYP](images/context4.png)

> [!Note]  
> Le icone possono essere assegnate anche in base a un'applicazione specifica.

 

## <a name="instructions"></a>Istruzioni

### <a name="step-1"></a>Passaggio 1:

Creare una sottochiave denominata **DefaultIcon** in una delle due posizioni seguenti:

-   Per un'assegnazione del tipo di file, **HKEY \_ classi \_ radice** \\ *. Extension*
-   Per l'assegnazione di un'applicazione, **HKEY \_ classi \_ radice** \\ *ProgID*

### <a name="step-2"></a>Passaggio 2:

Assegnare la sottochiave **DefaultIcon** un valore predefinito di tipo **reg \_ SZ** che specifica il percorso completo del file che contiene l'icona.

### <a name="step-3"></a>Passaggio 3:

Chiamare la funzione [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) per notificare alla shell di aggiornare la cache delle icone.

## <a name="remarks"></a>Commenti

Nell'esempio seguente viene illustrata una visualizzazione dettagliata delle voci del registro di sistema necessarie per l'assegnazione di un'icona di tipo file. L'estensione del nome file è associata a un'applicazione, ma l'assegnazione dell'icona è all'estensione del nome file, in modo che l'applicazione associata non stabilisca l'icona predefinita.

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
      DefaultIcon
         (Default) = C:\MyDir\MyProgram.exe,2
```

Nell'esempio seguente viene illustrata una visualizzazione dettagliata delle voci del registro di sistema necessarie per l'assegnazione di un'icona dell'applicazione. L'estensione del nome di file. MYP viene prima associata all'applicazione Program. 1. Alla sottochiave ProgID Program. 1 viene quindi assegnata l'icona predefinita personalizzata.

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   MyProgram.1
      DefaultIcon
         (Default) = C:\MyDir\MyProgram.exe,2
```

Tutti i file che contengono un'icona sono accettabili, inclusi i file ICO, exe e dll. Se nel file è presente più di un'icona, il percorso deve essere seguito da una virgola e quindi dall'indice dell'icona.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di file](fa-file-types.md)
</dt> </dl>

 

 



