---
title: Uso di MIDL
description: Creazione e compilazione di un'interfaccia Microsoft Interface Definition Language (MIDL) e RPC (Remote Procedure Call).
ms.assetid: 2594e3d6-d44a-4e12-8286-b9700e67702e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5ae89a740831fef28ade4c07dc6bbe2b9b68a8a154eb119f47e16b2cb68b325
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010749"
---
# <a name="using-midl"></a>Uso di MIDL

Tutte le interfacce per i programmi che usano RPC devono essere definite in Microsoft Interface Definition Language (MIDL) e compilate con il compilatore MIDL. Gli argomenti seguenti presentano una breve panoramica della creazione e della compilazione di un'interfaccia MIDL:

-   [Definizione di un'interfaccia con MIDL](#defining-an-interface-with-midl)
-   [Compilazione di un file MIDL](#compiling-a-midl-file)

Per una descrizione dettagliata di questi argomenti, vedere [File IDL e ACF.](the-idl-and-acf-files.md)

## <a name="defining-an-interface-with-midl"></a>Definizione di un'interfaccia con MIDL

I file MIDL sono file di testo che è possibile creare e modificare con un editor di testo. Se si genera un UUID per l'interfaccia, in genere si archivia l'output in un file MIDL modello. Per altre informazioni sugli UUID, vedere [Generating Interface UUIDs](generating-interface-uuids.md).

Tutte le interfacce in MIDL seguono lo stesso formato. Iniziano con un'intestazione che contiene un elenco di attributi di interfaccia e il nome dell'interfaccia. Gli attributi sono racchiusi tra parentesi quadre. L'intestazione dell'interfaccia è seguita dal corpo, racchiuso tra parentesi graffe. Nell'esempio seguente viene illustrata un'interfaccia semplice:

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

Alcuni degli attributi in genere presenti in una definizione di interfaccia MIDL sono l'UUID e il numero di versione dell'interfaccia. Il corpo della definizione dell'interfaccia deve contenere le dichiarazioni di routine di tutte le procedure remote nell'interfaccia. Può inoltre contenere le dichiarazioni dei tipi di dati e delle costanti richieste dall'interfaccia .

Tutti i parametri nelle dichiarazioni di procedura remota devono essere dichiarati \[ [**come in**](/windows/desktop/Midl/in) \] , \[ [**out**](/windows/desktop/Midl/out-idl) \] o \[ **in**, **out** \] . Queste dichiarazioni specificano che il programma client passa i dati in una procedura remota, ottiene i dati da una procedura remota o entrambi. Per informazioni più dettagliate sulle dichiarazioni dei parametri di interfaccia, vedere [Corpo dell'interfaccia IDL.](the-idl-interface-body.md)

## <a name="compiling-a-midl-file"></a>Compilazione di un file MIDL

Il compilatore MIDL è uno strumento da riga di comando che viene installato automaticamente con Platform Software Development Kit (SDK). Richiamarlo in una finestra di comando digitando il comando **midl**, seguito dal nome di un file MIDL, nella riga di comando. Verificare che la directory contenente il compilatore MIDL si trova nel percorso. L'esempio seguente ne illustra l'uso:

**midl MyApp.idl**

Si noti che non è necessario includere l'estensione se il nome file ha l'estensione idl. È anche possibile usare [](/windows/desktop/Midl/midl-command-line-reference) le opzioni della riga di comando del compilatore MIDL inserendole tra il **comando midl** e il nome del file. Questa operazione è illustrata nell'esempio seguente:

**midl /acf MyApp.acf MyApp.idl**

In questo esempio il compilatore MIDL viene eseguito usando il file MyApp.idl come file di input. L'opzione della riga di comando **/acf** indica al compilatore di usare anche un file di configurazione dell'applicazione (ACF) per l'input. I file di configurazione dell'applicazione sono descritti in modo più approfondito in [File IDL e ACF.](the-idl-and-acf-files.md)

Per informazioni più dettagliate sull'uso del compilatore MIDL, vedere Microsoft Interface Definition Language [(MIDL)](/windows/desktop/Midl/midl-start-page), che contiene informazioni sugli argomenti seguenti:

-   [Requisiti del preprocessore C per MIDL](/windows/desktop/Midl/c-preprocessor-requirements-for-midl)
-   [Considerazioni sul compilatore C/C++](/windows/desktop/Midl/c-c-compiler-considerations)
-   [File generati per un'interfaccia RPC](/windows/desktop/Midl/files-generated-for-an-rpc-interface)
-   [MIDL Command-line Reference](/windows/desktop/Midl/midl-command-line-reference)
-   [Informazioni di riferimento sul linguaggio MIDL](/windows/desktop/Midl/midl-language-reference)
-   [Errori e avvisi del compilatore MIDL](/windows/desktop/Midl/midl-compiler-errors-and-warnings)

 

 