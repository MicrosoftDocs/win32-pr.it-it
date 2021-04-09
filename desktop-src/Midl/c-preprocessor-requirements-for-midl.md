---
title: C-requisiti per il preprocessore MIDL
description: Questa pagina è valida solo per gli sviluppatori che hanno motivi specifici per sostituire il preprocessore Microsoft C/C++ come preprocessore utilizzato da MIDL o per sviluppatori che devono specificare opzioni personalizzate per il preprocessore.
ms.assetid: 1dd5eef4-5ea4-4958-8f53-9a95c0ccbf3e
keywords:
- MIDL compilatore MIDL, C-preprocessore, requisiti
- C-preprocessore MIDL, requisiti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b49c4e0c086a52eda2705d72cf2a2ff22c759290
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955697"
---
# <a name="c-preprocessor-requirements-for-midl"></a>C-requisiti per il preprocessore MIDL

Questa pagina è valida solo per gli sviluppatori che hanno motivi specifici per sostituire il preprocessore Microsoft C/C++ come preprocessore utilizzato da MIDL o per sviluppatori che devono specificare opzioni personalizzate per il preprocessore. I commutatori MIDL [**/cpp \_ cmd**](-cpp-cmd.md), [**/cpp \_ opt**](-cpp-opt.md)e [**/No \_ cpp**](-no-cpp-nocpp.md) vengono usati per eseguire l'override del comportamento predefinito del compilatore. Non esiste in genere un motivo per sostituire il preprocessore Microsoft C/C++, né per specificare opzioni per il preprocessore personalizzate.

Il compilatore MIDL usa un preprocessore C durante l'elaborazione iniziale del file IDL. L'ambiente di compilazione utilizzato per la compilazione dei file IDL è associato a un preprocessore di C/C++ predefinito. Se è necessario usare un preprocessore diverso, l'opzione del compilatore MIDL [**/cpp \_ cmd**](-cpp-cmd.md) Abilita un override del nome predefinito del preprocessore C/C++:

``` syntax
midl /cpp_cmd preprocessor_name filename
```

<dl> <dt>

<span id="preprocessor_name"></span><span id="PREPROCESSOR_NAME"></span>*nome del preprocessore \_*
</dt> <dd>

Specifica il nome del preprocessore che deve essere usato da MIDL. Può essere specificato con un percorso del file binario. L'estensione exe è facoltativa.

</dd> <dt>

<span id="filename"></span><span id="FILENAME"></span>*filename*
</dt> <dd>

Specifica il nome del file IDL.

</dd> </dl>

-   Il compilatore MIDL prevede che qualsiasi preprocessore osservi le convenzioni seguenti:
-   Il file di input viene specificato come ultimo argomento nella riga di comando.
-   Il preprocessore deve reindirizzare l'output al dispositivo di output standard, stdout.
-   Nel flusso di output del preprocessore sono presenti le direttive **\# line** che consentono di migliorare i messaggi di diagnostica.
-   Le direttive line sono le uniche direttive per il preprocessore nel flusso di output.

MIDL presuppone che il preprocessore generato abbia rimosso tutte le direttive del preprocessore dal flusso di input del compilatore, fatta eccezione per le occorrenze della direttiva di riga necessaria per individuare il percorso di origine nei messaggi del compilatore. Quando viene indicato un preprocessore diverso dal preprocessore Microsoft C/C++ o quando si specificano le opzioni del preprocessore con l'opzione [**/cpp \_ opt**](-cpp-opt.md) , è necessario specificare un'opzione del preprocessore appropriata che inserisce le direttive di riga nel flusso di input del compilatore. Per il preprocessore Microsoft C/C++, ad esempio, è necessario usare l'opzione **/e** :

``` syntax
midl /cpp_cmd cl.exe /cpp_opt "/E" file.idl
```

La direttiva **\# line** viene accettata da MIDL in uno dei formati seguenti:

``` syntax
#line digit-sequence "filename" new-line
 
# digit-sequence "filename" new-line
```

Per una descrizione completa della direttiva line e di altre direttive per il preprocessore, vedere la documentazione relativa al compilatore C usato.

MIDL accetta solo la direttiva per il preprocessore line. Di conseguenza, se si usa l'opzione [**\_ cpp/no**](-no-cpp-nocpp.md) , il file di input non deve avere altre direttive per il preprocessore oppure il file di input deve essere stato elaborato prima di richiamare MIDL.

Per ulteriori informazioni, vedere la pagina relativa alla [gestione delle \# definizioni nei file IDL](dealing-with-defines-in-idl-files-2.md).

 

 




