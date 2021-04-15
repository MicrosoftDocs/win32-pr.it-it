---
title: Componenti di MIDLRT e Windows Runtime
description: Viene illustrato come creare i file di metadati (con estensione winmd) che rappresentano l'API per i componenti Windows Runtime personalizzati.
ms.assetid: 7830A5DB-9696-4A93-948B-51DA46A5143C
keywords:
- MIDL compilatore MIDL
- MIDL Compiler MIDL, MIDL e Windows Runtime WinRT
- Windows Runtime MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4edf4d40b3fc5b0a5ed8eeb9b5fd47a3b87c4543
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104517217"
---
# <a name="midlrt-and-windows-runtime-components"></a>Componenti di MIDLRT e Windows Runtime

Viene illustrato come creare i file di metadati (con estensione winmd) che rappresentano l'API per i componenti Windows Runtime personalizzati.


Usare il compilatore MIDLRT per compilare file di metadati (con estensione winmd) per i componenti Windows Runtime personalizzati.

Quando vengono generati i file di metadati, è possibile comprimerli in un pacchetto più efficiente tramite l'utilità MDMERGE. Per altre informazioni, vedere [MDMERGE e file di metadati](mdmerge-and-metadata-files.md).


L'uso di MIDLRT è simile all'uso del compilatore MIDL. Eseguire MIDLRT dalla riga di comando usando il comando seguente:

**midlrt**  *<* **Opzioni** _>_ di **filename. idl**

dove * < ***Opzioni** _>_ rappresenta le opzioni della riga di comando che si desidera utilizzare e filename. idl è il nome del file IDL da compilare.


Nell'elenco seguente vengono illustrate le opzioni della riga di comando utilizzate da MIDLRT.EXE.

<dl>

[**\_classe/enum**](-enum-class.md)  
[**\_dir/Metadata**](-metadata-dir.md)  
[**/nomidl**](-nomidl.md)  
[**/nomd**](-nomd.md)  
[**\_prefisso/NS**](-ns-prefix.md)  
[**/WinMD**](-winmd.md)  
[**/WinRT**](-winrt.md)  
</dl>

Un elenco completo delle opzioni e delle opzioni del compilatore MIDLRT è disponibile quando si usa il compilatore MIDLRT [**/Help**](-help-.md) e/? interruttori. Le opzioni sono organizzate in base alle categorie. Per altre informazioni, vedere la Guida di [riferimento a MIDL Command-Line](midl-command-line-reference.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[MDMERGE e file di metadati](mdmerge-and-metadata-files.md)
</dt> </dl>

 

 




