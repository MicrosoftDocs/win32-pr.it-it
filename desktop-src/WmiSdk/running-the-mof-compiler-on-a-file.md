---
description: "Durante la compilazione di un file MOF sono disponibili due opzioni: l'uso dell'utilità della riga di comando o l'uso di un'interfaccia a livello di codice."
ms.assetid: 1760f1bd-7027-4201-97a2-ca902f945b52
ms.tgt_platform: multiple
title: Esecuzione del compilatore MOF in un file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1a70c32e82b826f2ab02403e7e269e711704d826ad4b4f9465638df0b0745f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050329"
---
# <a name="running-the-mof-compiler-on-a-file"></a>Esecuzione del compilatore MOF in un file

Durante la compilazione di un file MOF sono disponibili due opzioni: l'uso dell'utilità della riga di comando o l'uso di un'interfaccia a livello di codice.

Fino a quando non si esegue il compilatore MOF, [**Mofcomp.exe**](mofcomp.md), un provider non è registrato con WMI e le classi create nel file MOF non sono disponibili nel [*repository WMI*](gloss-w.md). La procedura seguente descrive come compilare un file MOF.

**Per eseguire il compilatore MOF in un file dalla riga di comando**

1.  Chiamare il compilatore MOF dalla riga di comando usando la sintassi seguente.

    **mofcomp** _MOFfile_**.mof**

    Il compilatore MOF supporta un'ampia gamma di opzioni per controllare situazioni di elaborazione speciali. Tutte le opzioni sono facoltative ed è consentita qualsiasi combinazione di opzioni. Tuttavia, non ha senso usare alcune opzioni in combinazione con altre. Ad esempio, per combinare le opzioni **-class:updateonly** e **-class:createonly,** il compilatore non esegue alcuna azione.

    Per impostazione predefinita, Mofcomp.exe le classi compilate nello spazio dei \\ nomi WMI predefinito radice. Si noti che lo spazio dei nomi predefinito Mofcomp.exe non corrisponde allo spazio dei nomi predefinito per lo scripting. Lo spazio dei nomi predefinito per lo scripting viene specificato nel controllo WMI nella scheda Avanzate . Per altre informazioni, vedere [Impostazione della sicurezza dello spazio dei nomi con il controllo WMI.](setting-namespace-security-with-the-wmi-control.md)

    È possibile modificare lo spazio dei nomi che riceve le classi in due modi.

    1.  Usare **l'opzione -N** per il **comando mofcomp.**
    2.  Inserire lo spazio dei nomi pragma del \# [**comando del**](pragma-namespace.md) preprocessore nel file MOF.

2.  Facoltativamente, è possibile compilare un file MOF a livello di codice. Per altre informazioni, vedere [**IMofCompiler.**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Compilazione di file MOF](compiling-mof-files.md)
</dt> <dt>

[**mofcomp**](mofcomp.md)
</dt> <dt>

[Comandi del preprocessore](preprocessor-commands.md)
</dt> </dl>

 

 



