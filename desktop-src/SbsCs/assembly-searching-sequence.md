---
description: Se un'applicazione isolata specifica una dipendenza dell'assembly, l'assembly viene innanzitutto ricercato side-by-side tra gli assembly condivisi nella cartella WinSxS.
ms.assetid: 93496631-55cc-4dd9-9a51-b748c35fd477
title: Sequenza di ricerca di assembly
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 983466954d6cb9619d3fb0595c96f81fed7c9b73a29bfbf2f609b3f14203a957
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127541"
---
# <a name="assembly-searching-sequence"></a>Sequenza di ricerca di assembly

Se un'applicazione isolata specifica una dipendenza dell'assembly, l'assembly [](/windows/desktop/Msi/shared-assemblies) viene innanzitutto ricercato side-by-side tra gli assembly condivisi nella cartella WinSxS. Se l'assembly richiesto non viene trovato, viene eseguita la ricerca affiancata di un assembly privato installato in una cartella della struttura di directory dell'applicazione.

[Gli assembly privati](/windows/desktop/Msi/private-assemblies) possono essere distribuiti nei percorsi seguenti nella struttura di directory dell'applicazione:

-   Nella cartella dell'applicazione. In genere, si tratta della cartella contenente il file eseguibile dell'applicazione.
-   In una sottocartella nella cartella dell'applicazione. La sottocartella deve avere lo stesso nome dell'assembly.
-   In una sottocartella specifica della lingua nella cartella dell'applicazione. Il nome della sottocartella è una stringa di codici di lingua DHTML che indica una lingua o impostazioni cultura.
-   In una sottocartella di una sottocartella specifica della lingua nella cartella dell'applicazione. Il nome della sottocartella superiore è una stringa di codici di lingua DHTML che indica una lingua o una lingua. La sottocartella più profonda ha lo stesso nome dell'assembly.

La prima volta che viene eseguita una ricerca side-by-side di un assembly privato, determina se nella struttura di directory dell'applicazione è presente una sottocartella specifica della lingua. Se non esiste alcuna sottocartella specifica del linguaggio, l'assembly privato viene ricercato side-by-side nei percorsi seguenti usando la sequenza seguente.

1.  La ricerca affiancata viene eseguita nella cartella WinSxS.
2.  \\\\< > \\ appdir < *nome assembly*>.DLL
3.  \\\\< > \\ appdir < *assemblyname*>.manifest
4.  \\\\< > \\ appdir < *nome assembly* > \\ < *nome assembly*>.DLL
5.  \\\\< > \\ appdir < *nome assembly* > \\ < *assemblyname*>.manifest

Se esiste una sottocartella specifica della lingua, la struttura di directory dell'applicazione può contenere l'assembly privato localizzato in più lingue. Esegue una ricerca side-by-side nelle sottocartelle specifiche della lingua per assicurarsi che l'applicazione usi la lingua specificata o la lingua migliore disponibile. Le sottocartelle specifiche della lingua vengono denominate usando una stringa di codici di lingua DHTML che specificano una lingua o una lingua. Se esiste una sottocartella specifica del linguaggio, l'assembly privato viene ricercato side-by-side nei percorsi seguenti usando la sequenza seguente.

1.  La ricerca affiancata viene eseguita nella cartella WinSxS.
2.  \\\\< > \\ appdir < *language-culture* > \\ < *nome assembly*>.DLL
3.  \\\\< > \\ appdir < *language-culture* > \\ < *assemblyname*>.manifest
4.  \\\\< > \\ appdir < *language-culture* > \\ < *nome assembly* > \\ < *nome assembly*>.DLL
5.  \\\\< > \\ appdir < *language-culture* > \\ < *nome assembly* > \\ < *assemblyname*>.manifest

Si noti che la sequenza di ricerca side-by-side trova un file DLL con il nome dell'assembly e si arresta prima di cercare un file manifesto con il nome dell'assembly. Il modo consigliato per gestire un assembly privato che è una DLL è inserire il manifesto dell'assembly nel file DLL come risorsa. L'ID risorsa deve essere uguale a 1 e il nome dell'assembly privato può corrispondere al nome della DLL. Ad esempio, se il nome della DLL è MICROSOFT.WINDOWS.MYSAMPLE.DLL, anche il valore dell'attributo name usato nell'elemento **assemblyIdentity** del manifesto dell'assembly può essere Microsoft. Windows.mysample. In alternativa, è possibile inserire il manifesto dell'assembly in un file separato, ma il nome dell'assembly e il relativo manifesto devono essere diversi dal nome della DLL. Ad esempio, Microsoft. Windows.mysampleAsm, Microsoft. Windows.mysampleAsm.manifest e MICROSOFT.WINDOWS.MYSAMPLE.DLL.

Ad esempio, se myapp è installato nella radice dell'unità c: e richiede myasm in Francese-Emigrante, side-by-side usa la sequenza seguente per cercare la migliore approssimazione a un'istanza localizzata di myasm.

1.  Side-by-side cerca in WinSxS la versione fr-be.
2.  c: \\ myapp \\ fr-be \\myasm.dll
3.  c: \\ myapp \\ fr-be \\ myasm.manifest
4.  c: \\ myapp \\ fr-be \\ myasm \\myasm.dll
5.  c: \\ myapp \\ fr-be \\ myasm \\ myasm.manifest
6.  Side-by-side cerca in WinSxS la versione fr.
7.  c: \\ myapp \\ fr \\myasm.dll
8.  c: \\ myapp \\ fr \\ myasm.manifest
9.  c: \\ myapp \\ fr \\ myasm \\myasm.dll
10. c: \\ myapp \\ fr \\ myasm \\ myasm.manifest
11. Side-by-side cerca in WinSxS la versione en-us.
12. c: \\ myapp \\ en-us \\myasm.dll
13. c: \\ myapp \\ en-us \\ myasm.manifest
14. c: \\ myapp \\ en-us \\ myasm \\myasm.dll
15. c: \\ myapp \\ en-us \\ myasm \\ myasm.manifest
16. Side-by-side cerca la versione en in WinSxS.
17. c: \\ myapp \\ en \\myasm.dll
18. c: \\ myapp \\ en \\ myasm.manifest
19. c: \\ myapp \\ en \\ myasm \\myasm.dll
20. c: \\ myapp \\ en \\ myasm \\ myasm.manifest
21. Side-by-side cerca in WinSxS la versione senza lingua.
22. c: \\ myapp \\myasm.dll
23. c: \\ myapp \\ myasm.manifest
24. c: \\ myapp \\ myasm \\myasm.dll
25. c: \\ myapp \\ myasm \\ myasm.manifest

Se la ricerca side-by-side raggiunge una versione indipendente dalla lingua dell'assembly e nel sistema è presente una versione [MUI (Multilanguage Interfaccia utente)](/windows/desktop/Intl/multilingual-user-interface) di Windows, viene eseguito un tentativo di associazione a <*nome assembly*>.mui. L'associazione side-by-side a <*assemblyname*>.mui se la ricerca raggiunge una versione localizzata dell'assembly. Il [manifesto dell'assembly](assembly-manifests.md) di un assembly indipendente dalla lingua non avrà un attributo language nell'elemento **assemblyIdentity.** Se l'esecuzione side-by-side raggiunge un assembly indipendente dalla lingua e MUI è installato, esegue una ricerca side-by-side nei percorsi seguenti usando la sequenza seguente per trovare <*nome assembly*>.mui. L'esecuzione side-by-side usa la stessa sequenza di ricerca se l'assembly è indipendente dalle impostazioni cultura, ad <*non* viene> lingua.

1.  La ricerca side-by-side nella cartella WinSxS <*assemblyname*>.mui.
2.  \\\\<*impostazioni cultura della lingua dell'utente* > \\ < *assemblyname*>.mui
3.  \\\\<*lingua dell'utente* > \\ < *assemblyname*>.mui
4.  \\\\<*impostazioni cultura della lingua del sistema* > \\ < *assemblyname*>.mui
5.  \\\\<*linguaggio del sistema* > \\ < *assemblyname*>.mui
6.  \\\\<*nessuna lingua* > \\ < *assemblyname*>.mui

Ad esempio, se la ricerca side-by-side trova l'assembly privato in c: \\ myapp \\ \\ myasm myasm.manifest e myasm è un assembly indipendente dalla lingua. Side-by-side usa quindi la sequenza seguente per cercare myasm.mui. Si noti che side-by-side non cerca un assembly MUI indipendente dalla lingua.

1.  Side-by-side cerca in WinSxS la versione fr-be dell'assembly MUI.
2.  c: \\ myapp \\ fr-be \\myasm.mui.dll
3.  c: \\ myapp \\ fr-be \\ myasm.mui.manifest
4.  c: \\ myapp \\ fr-be \\ myasm \\myasm.mui.dll
5.  c: \\ myapp \\ fr-be \\ myasm \\ myasm.mui.manifest
6.  Side-by-side cerca in WinSxS la versione fr dell'assembly MUI.
7.  c: \\ myapp \\ fr \\myasm.mui.dll
8.  c: \\ myapp \\ fr \\ myasm.mui.manifest
9.  c: \\ myapp \\ fr \\ myasm \\myasm.mui.dll
10. c: \\ myapp \\ fr \\ myasm \\ myasm.mui.manifest
11. Side-by-side cerca in WinSxS la versione en-us dell'assembly MUI.
12. c: \\ myapp \\ en-us \\myasm.mui.dll
13. c: \\ myapp \\ en-us \\ myasm.mui.manifest
14. c: \\ myapp \\ en-us \\ myasm \\myasm.mui.dll
15. c: \\ myapp \\ en-us \\ myasm \\ myasm.mui.manifest
16. Side-by-side cerca in WinSxS la versione en dell'assembly MUI.
17. c: \\ myapp \\ en \\myasm.mui.dll
18. c: \\ myapp \\ en \\ myasm.mui.manifest
19. c: \\ myapp \\ en \\ myasm \\myasm.mui.dll
20. c: \\ myapp \\ en \\ myasm \\ myasm.mui.manifest

 

 
