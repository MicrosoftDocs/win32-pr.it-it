---
title: Componenti MIDLRT e Windows Runtime
description: Illustra come creare file di metadati (con estensione winmd) che rappresentano l'API per i componenti Windows Runtime.
ms.assetid: 7830A5DB-9696-4A93-948B-51DA46A5143C
keywords:
- MIDL del compilatore MIDL
- MidL del compilatore MIDL, MIDL e Windows Runtime winrt
- Windows Runtime MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f827178216bbb7e78c16f2c11fa68b29b2eb50cfc0714a0ed53b02ce5bdc4ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118642905"
---
# <a name="midlrt-and-windows-runtime-components"></a>Componenti MIDLRT e Windows Runtime

Illustra come creare file di metadati (con estensione winmd) che rappresentano l'API per i componenti Windows Runtime.


Usare il compilatore MIDLRT per compilare file di metadati (con estensione winmd) per i componenti Windows Runtime.

Quando i file di metadati vengono generati, è possibile componirli in un pacchetto più efficiente usando l'utilità MDMERGE. Per altre informazioni, vedere [MDMERGE e i file di metadati.](mdmerge-and-metadata-files.md)


L'uso di MIDLRT è simile all'uso del compilatore MIDL. Eseguire MIDLRT dalla riga di comando usando il comando seguente:

**midlrt**  *<* **opzioni** _>_ **filename.idl**

dove *<***opzioni** rappresenta le opzioni della riga di comando da usare e Filename.idl è il nome del _>_ file IDL da compilare.


L'elenco seguente mostra le opzioni della riga di comando MIDLRT.EXE.

<dl>

[**Classe \_ /enum**](-enum-class.md)  
[**/metadata \_ dir**](-metadata-dir.md)  
[**/nomidl**](-nomidl.md)  
[**/nomd**](-nomd.md)  
[**Prefisso \_ /ns**](-ns-prefix.md)  
[**/winmd**](-winmd.md)  
[**/winrt**](-winrt.md)  
</dl>

Un elenco completo delle opzioni e delle opzioni del compilatore MIDLRT è disponibile quando si usa il compilatore MIDLRT [**/help**](-help-.md) e /? Interruttori. I commutatori sono organizzati in base alle categorie. Per altre informazioni, vedere [Midl Command-Line Reference](midl-command-line-reference.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[MDMERGE e file di metadati](mdmerge-and-metadata-files.md)
</dt> </dl>

 

 




