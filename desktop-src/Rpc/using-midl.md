---
title: Uso di MIDL
description: Creazione e compilazione di un'interfaccia Microsoft Interface Definition Language (MIDL) e RPC (Remote Procedure Call).
ms.assetid: 2594e3d6-d44a-4e12-8286-b9700e67702e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22da60f20cba6c558c7f1a67478adef7b407d591
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103730015"
---
# <a name="using-midl"></a>Uso di MIDL

Tutte le interfacce per i programmi che usano RPC devono essere definite in Microsoft Interface Definition Language (MIDL) e compilate con il compilatore MIDL. Negli argomenti seguenti viene presentata una breve panoramica sulla creazione e la compilazione di un'interfaccia MIDL:

-   [Definizione di un'interfaccia con MIDL](#defining-an-interface-with-midl)
-   [Compilazione di un file MIDL](#compiling-a-midl-file)

Per una descrizione dettagliata di questi argomenti, vedere [i file IDL e ACF](the-idl-and-acf-files.md).

## <a name="defining-an-interface-with-midl"></a>Definizione di un'interfaccia con MIDL

I file MIDL sono file di testo che è possibile creare e modificare con un editor di testo. Se si genera un UUID per l'interfaccia, in genere l'output viene archiviato in un file MIDL del modello. Per altre informazioni sugli UUID, vedere [generazione di UUID di interfaccia](generating-interface-uuids.md).

Tutte le interfacce in MIDL seguono lo stesso formato. Iniziano con un'intestazione contenente un elenco di attributi di interfaccia e il nome dell'interfaccia. Gli attributi sono racchiusi tra parentesi quadre. L'intestazione dell'interfaccia è seguita dal corpo, racchiuso tra parentesi graffe. Nell'esempio seguente viene illustrata un'interfaccia semplice:

``` syntax
[
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0)
]
interface MyInterface
{
  const unsigned short INT_ARRAY_LEN = 100;

  void MyRemoteProc( 
      [in] int param1,
      [out] int outArray[INT_ARRAY_LEN]
  );
}
```

Alcuni degli attributi che in genere compaiono in una definizione di interfaccia MIDL sono UUID e il numero di versione dell'interfaccia. Il corpo della definizione dell'interfaccia deve contenere le dichiarazioni di routine di tutte le procedure remote nell'interfaccia. Può inoltre contenere le dichiarazioni dei tipi di dati e delle costanti richieste dall'interfaccia.

Tutti i parametri nelle dichiarazioni di procedura remota devono essere dichiarati come \[ [**in**](/windows/desktop/Midl/in) \] , \[ [**out**](/windows/desktop/Midl/out-idl) \] o \[ **in**, **out** \] . Queste dichiarazioni specificano che il programma client passa i dati in una procedura remota, ottiene i dati da una procedura remota o entrambi. Per informazioni più dettagliate sulle dichiarazioni dei parametri di interfaccia, vedere [il corpo dell'interfaccia IDL](the-idl-interface-body.md).

## <a name="compiling-a-midl-file"></a>Compilazione di un file MIDL

Il compilatore MIDL è uno strumento da riga di comando che viene installato automaticamente con Platform Software Development Kit (SDK). Richiamarlo in una finestra di comando digitando il comando **MIDL**, seguito dal nome di un file MIDL, nella riga di comando. Assicurarsi che la directory contenente il compilatore MIDL si trovi nel percorso. Nell'esempio seguente viene illustrato l'utilizzo di:

**MIDL MyApp. idl**

Si noti che non è necessario includere l'estensione se il nome file ha l'estensione. idl. È anche possibile usare le opzioni della [riga di comando](/windows/desktop/Midl/midl-command-line-reference) del compilatore MIDL inserendole tra il comando **MIDL** e il nome del file. Questa operazione è illustrata nell'esempio seguente:

**MIDL/ACF MyApp. ACF MyApp. idl**

In questo esempio, il compilatore MIDL viene eseguito utilizzando il file MyApp. idl come file di input. L'opzione della riga di comando **/ACF** indica al compilatore di usare un file di configurazione dell'applicazione (ACF) anche per l'input. I file di configurazione dell'applicazione sono trattati più accuratamente nei [file IDL e ACF](the-idl-and-acf-files.md).

Per informazioni più dettagliate sull'uso del compilatore MIDL, vedere il [Microsoft Interface Definition Language (MIDL)](/windows/desktop/Midl/midl-start-page), che contiene informazioni sugli argomenti seguenti:

-   [C-requisiti per il preprocessore MIDL](/windows/desktop/Midl/c-preprocessor-requirements-for-midl)
-   [C/C++-considerazioni sul compilatore](/windows/desktop/Midl/c-c-compiler-considerations)
-   [File generati per un'interfaccia RPC](/windows/desktop/Midl/files-generated-for-an-rpc-interface)
-   [Riferimenti alla riga di comando MIDL](/windows/desktop/Midl/midl-command-line-reference)
-   [Riferimenti per il linguaggio MIDL](/windows/desktop/Midl/midl-language-reference)
-   [Errori e avvisi del compilatore MIDL](/windows/desktop/Midl/midl-compiler-errors-and-warnings)

 

 