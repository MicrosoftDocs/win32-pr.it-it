---
description: Se un'applicazione isolata specifica una dipendenza di assembly, viene innanzitutto eseguita una ricerca side-by-side dell'assembly tra gli assembly condivisi nella cartella WinSxS.
ms.assetid: 93496631-55cc-4dd9-9a51-b748c35fd477
title: Sequenza di ricerca degli assembly
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc689ecb14c55f0e8a609c7e7497fce969e88b8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050248"
---
# <a name="assembly-searching-sequence"></a>Sequenza di ricerca degli assembly

Se un'applicazione isolata specifica una dipendenza di assembly, viene innanzitutto eseguita una ricerca side-by-side dell'assembly tra gli [assembly condivisi](/windows/desktop/Msi/shared-assemblies) nella cartella WinSxS. Se l'assembly richiesto non viene trovato, Side-by-side Cerca un assembly privato installato in una cartella della struttura di directory dell'applicazione.

Gli [assembly privati](/windows/desktop/Msi/private-assemblies) possono essere distribuiti nei percorsi seguenti nella struttura di directory dell'applicazione:

-   Nella cartella dell'applicazione. Si tratta in genere della cartella che contiene il file eseguibile dell'applicazione.
-   In una sottocartella della cartella dell'applicazione. La sottocartella deve avere lo stesso nome dell'assembly.
-   In una sottocartella specifica della lingua nella cartella dell'applicazione. Il nome della sottocartella è una stringa di codici di linguaggio DHTML che indica una lingua o una lingua.
-   In una sottocartella di una sottocartella specifica della lingua nella cartella dell'applicazione. Il nome della sottocartella più elevata è una stringa di codici di linguaggio DHTML che indica una lingua o una lingua. La sottocartella più profonda ha lo stesso nome dell'assembly.

La prima volta che si esegue la ricerca side-by-side di un assembly privato, determina se una sottocartella specifica del linguaggio è presente nella struttura di directory dell'applicazione. Se non esiste alcuna sottocartella specifica della lingua, Side-by-side cerca l'assembly privato nei percorsi seguenti usando la sequenza seguente.

1.  Side-by-side Cerca nella cartella WinSxS.
2.  \\\\< > \\ appdir < *AssemblyName* # C0.DLL
3.  \\\\< > \\ appdir < *assemblyname*>. manifest
4.  \\\\< > \\ appdir <  > \\ AssemblyName < *AssemblyName* # C0.DLL
5.  \\\\< > \\ appdir <  > \\ AssemblyName < *assemblyname*>. manifest

Se esiste una sottocartella specifica della lingua, la struttura di directory dell'applicazione può contenere l'assembly privato localizzato in più lingue. Side-by-side Cerca le sottocartelle specifiche della lingua per assicurarsi che l'applicazione usi la lingua specificata o la migliore lingua disponibile. Le sottocartelle specifiche della lingua vengono denominate utilizzando una stringa di codici di linguaggio DHTML che specificano una lingua o una lingua. Se esiste una sottocartella specifica della lingua, Side-by-side cerca l'assembly privato nei percorsi seguenti usando la sequenza seguente.

1.  Side-by-side Cerca nella cartella WinSxS.
2.  \\\\< > \\ appdir < *lingua-impostazioni cultura* > \\ < *AssemblyName* # C0.DLL
3.  \\\\< > \\ appdir < *lingua-impostazioni cultura* > \\ < *assemblyname*>. manifest
4.  \\\\< > \\ appdir < *lingua-impostazioni cultura* > \\ <  > \\ AssemblyName < *AssemblyName* # C0.DLL
5.  \\\\< > \\ appdir < *lingua-impostazioni cultura* > \\ <  > \\ AssemblyName < *assemblyname*>. manifest

Si noti che la sequenza di ricerca affiancata consente di trovare un file DLL con il nome dell'assembly e si arresta prima di cercare un file manifesto con il nome dell'assembly. Il metodo consigliato per gestire un assembly privato che è una DLL è inserire il manifesto dell'assembly nel file DLL come risorsa. L'ID risorsa deve essere uguale a 1 e il nome dell'assembly privato può corrispondere al nome della DLL. Se, ad esempio, il nome della DLL è MICROSOFT.WINDOWS.MYSAMPLE.DLL, il valore dell'attributo Name usato nell'elemento **assemblyIdentity** del manifesto dell'assembly può essere anche Microsoft. Windows. di esempio. In alternativa, è possibile inserire il manifesto dell'assembly in un file separato. Tuttavia, il nome dell'assembly e il relativo manifesto devono essere diversi dal nome della DLL. Ad esempio, Microsoft. Windows. mysampleAsm, Microsoft. Windows. mysampleAsm. manifest e MICROSOFT.WINDOWS.MYSAMPLE.DLL.

Ad esempio, se MyApp viene installato alla radice dell'unità c: e richiede MyAsm in francese-belga, Side-by-side usa la sequenza seguente per cercare la migliore approssimazione a un'istanza localizzata di MyAsm.

1.  Ricerche side-by-side WinSxS per la versione fr-be.
2.  c: \\ MyApp \\ fr-be \\myasm.dll
3.  c: \\ MyApp \\ fr-be \\ MyAsm. manifest
4.  c: \\ MyApp \\ fr-be \\ MyAsm \\myasm.dll
5.  c: \\ MyApp \\ fr-be \\ MyAsm \\ MyAsm. manifest
6.  Ricerche side-by-side WinSxS per la versione FR.
7.  c: \\ MyApp \\ fr \\myasm.dll
8.  c: \\ MyApp \\ fr \\ MyAsm. manifest
9.  c: \\ MyApp \\ fr \\ MyAsm \\myasm.dll
10. c: \\ MyApp \\ fr \\ MyAsm \\ MyAsm. manifest
11. Ricerche side-by-side WinSxS per la versione en-US.
12. c: \\ MyApp \\ en-US \\myasm.dll
13. c: \\ MyApp \\ en-US \\ MyAsm. manifest
14. c: \\ MyApp \\ en-us \\ MyAsm \\myasm.dll
15. c: \\ MyApp \\ en-US \\ MyAsm \\ MyAsm. manifest
16. Ricerche side-by-side WinSxS per la versione en.
17. c: \\ MyApp \\ en \\myasm.dll
18. c: \\ MyApp \\ en \\ MyAsm. manifest
19. c: \\ MyApp \\ en \\ MyAsm \\myasm.dll
20. c: \\ MyApp \\ en \\ MyAsm \\ MyAsm. manifest
21. Ricerche side-by-side WinSxS per la versione nessuna lingua.
22. c: \\ myapp \\myasm.dll
23. c: \\ MyApp \\ MyAsm. manifest
24. c: \\ MyApp \\ MyAsm \\myasm.dll
25. c: \\ MyApp \\ MyAsm \\ MyAsm. manifest

Se la ricerca side-by-side raggiunge una versione dell'assembly indipendente dalla lingua e una versione [MUI (Multilingual User Interface)](/windows/desktop/Intl/multilingual-user-interface) di Windows è presente nel sistema, Side-by-side tenta di eseguire l'associazione a <*AssemblyName*>. mui. Side-by-side non tenta di eseguire l'associazione a <*assemblyname*>. mui se la ricerca raggiunge una versione localizzata dell'assembly. Il [manifesto dell'assembly](assembly-manifests.md) di un assembly indipendente dalla lingua non avrà un attributo Language nell'elemento **assemblyIdentity** . Se il percorso affiancato raggiunge un assembly indipendente dalla lingua ed è installato MUI, Side-by-side Cerca nei percorsi seguenti la seguente sequenza per <*assemblyname*>. mui. Side-by-side usa la stessa sequenza di ricerca se l'assembly è indipendente dalle impostazioni cultura, tranne <non viene eseguita la ricerca di> di *lingua* .

1.  Side-by-side Cerca nella cartella WinSxS il <*assemblyname*>. mui.
2.  \\\\<*lingua dell'utente-impostazioni cultura* > \\ < *assemblyname*>. mui
3.  \\\\< > lingua \\ dell' < utente *assemblyname*>. mui
4.  \\\\<*lingua del sistema-impostazioni cultura* > \\ < *assemblyname*>. mui
5.  \\\\< > lingua \\ del < sistema *assemblyname*>. mui
6.  \\\\<*Nessuna* > \\ lingua < *assemblyname*>. mui

Se, ad esempio, la ricerca side-by-side trova l'assembly privato in c: \\ MyApp \\ MyAsm \\ MyAsm. manifest e MyAsm è un assembly indipendente dal linguaggio. Side-by-side usa quindi la sequenza seguente per cercare MyAsm. mui. Si noti che side-by-side non cerca un assembly MUI indipendente dalla lingua.

1.  Ricerche side-by-side WinSxS per la versione fr-be dell'assembly MUI.
2.  c: \\ MyApp \\ fr-be \\myasm.mui.dll
3.  c: \\ MyApp \\ fr-be \\ MyAsm. mui. manifest
4.  c: \\ MyApp \\ fr-be \\ MyAsm \\myasm.mui.dll
5.  c: \\ MyApp \\ fr-be \\ MyAsm \\ MyAsm. mui. manifest
6.  Ricerche side-by-side WinSxS per la versione FR dell'assembly MUI.
7.  c: \\ MyApp \\ fr \\myasm.mui.dll
8.  c: \\ MyApp \\ fr \\ MyAsm. mui. manifest
9.  c: \\ MyApp \\ fr \\ MyAsm \\myasm.mui.dll
10. c: \\ MyApp \\ fr \\ MyAsm \\ MyAsm. mui. manifest
11. Ricerche side-by-side WinSxS per la versione en-US dell'assembly MUI.
12. c: \\ MyApp \\ en-US \\myasm.mui.dll
13. c: \\ MyApp \\ en-US \\ MyAsm. mui. manifest
14. c: \\ MyApp \\ en-us \\ MyAsm \\myasm.mui.dll
15. c: \\ MyApp \\ en-US \\ MyAsm \\ MyAsm. mui. manifest
16. Ricerche side-by-side WinSxS per la versione en dell'assembly MUI.
17. c: \\ MyApp \\ en \\myasm.mui.dll
18. c: \\ MyApp \\ en \\ MyAsm. mui. manifest
19. c: \\ MyApp \\ en \\ MyAsm \\myasm.mui.dll
20. c: \\ MyApp \\ en \\ MyAsm \\ MyAsm. mui. manifest

 

 
