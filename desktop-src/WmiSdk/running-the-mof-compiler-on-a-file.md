---
description: "Per la compilazione di un file MOF sono disponibili due opzioni: utilizzo dell'utilità da riga di comando o di un'interfaccia a livello di codice."
ms.assetid: 1760f1bd-7027-4201-97a2-ca902f945b52
ms.tgt_platform: multiple
title: Esecuzione del compilatore MOF in un file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad1605544e05f59670f9e6fd73fcd8c01862b46c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226830"
---
# <a name="running-the-mof-compiler-on-a-file"></a>Esecuzione del compilatore MOF in un file

Per la compilazione di un file MOF sono disponibili due opzioni: utilizzo dell'utilità da riga di comando o di un'interfaccia a livello di codice.

Fino a quando non si esegue il compilatore MOF, [**Mofcomp.exe**](mofcomp.md), un provider non è registrato con WMI e le classi create nel file MOF non sono disponibili nel [*repository WMI*](gloss-w.md). Nella procedura seguente viene descritto come compilare un file MOF.

**Per eseguire il compilatore MOF in un file dalla riga di comando**

1.  Chiamare il compilatore MOF dalla riga di comando, usando la sintassi seguente.

    **mofcomp** *MOFfile * * *. mof**

    Il compilatore MOF supporta un'ampia gamma di opzioni per il controllo di particolari situazioni di elaborazione. Tutte le opzioni sono facoltative ed è consentita qualsiasi combinazione di opzioni. Tuttavia, non ha senso usare alcuni dei commutatori in combinazione con altri. Ad esempio, per combinare le opzioni **-Class: updateonly** e **-Class: createonly** i risultati del compilatore non eseguono alcuna azione.

    Per impostazione predefinita, Mofcomp.exe archivia le classi compilate nello \\ spazio dei nomi WMI predefinito radice. Si noti che lo spazio dei nomi predefinito per Mofcomp.exe non corrisponde allo spazio dei nomi predefinito per lo scripting. Lo spazio dei nomi predefinito per lo scripting è specificato nel controllo WMI nella scheda Avanzate. Per ulteriori informazioni, vedere [impostazione della sicurezza dello spazio dei nomi con il controllo WMI](setting-namespace-security-with-the-wmi-control.md).

    È possibile modificare lo spazio dei nomi che riceve le classi in due modi.

    1.  Utilizzare l'opzione **-N** per il comando **mofcomp** .
    2.  Inserire lo \# [**spazio dei nomi pragma**](pragma-namespace.md) del comando per il preprocessore nel file MOF.

2.  Facoltativamente, è possibile compilare un file MOF a livello di codice. Per ulteriori informazioni, vedere [**IMOFCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Compilazione di file MOF](compiling-mof-files.md)
</dt> <dt>

[**mofcomp**](mofcomp.md)
</dt> <dt>

[Comandi del preprocessore](preprocessor-commands.md)
</dt> </dl>

 

 



