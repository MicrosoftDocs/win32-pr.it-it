---
description: Pktextract.exe è uno strumento che estrae l'attributo publicKeyToken da un file di certificato.
ms.assetid: 195ff5bd-bb60-4053-9308-ceacd29853c0
title: Pktextract.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e7f2cbb210262a05839ac3a7df71f3bedea603a5ea959249867efc2d5e420e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119884955"
---
# <a name="pktextractexe"></a>Pktextract.exe

Pktextract.exe è uno strumento che estrae **l'attributo publicKeyToken** da un file di certificato. L'output è **publicKeyToken,** ovvero un identificatore univoco a 16 caratteri (8 byte) della chiave pubblica presente nel certificato, in un formato che può essere incollato facilmente in un'istruzione di identità dell'assembly. Il file del certificato deve essere presente nella stessa directory Pktextract.exe usare l'utilità . Pktextract.exe è disponibile in Microsoft Windows Software Development Kit (SDK).

## <a name="syntax"></a>Sintassi

**pktextract.exe** *<filename.cer>* **\[ -quiet \] \[ -nologo \]**

## <a name="command-line-options"></a>Opzioni da riga di comando

Pktextract.exe usa le opzioni della riga di comando senza distinzione tra maiuscole e minuscole seguenti.



| Opzione  | Descrizione                                                          |
|---------|----------------------------------------------------------------------|
| -quiet  | Elimina la visualizzazione completa delle informazioni sul certificato. facoltativo.        |
| -nologo | Viene eseguito senza visualizzare i dati standard sul copyright Microsoft. facoltativo. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Strumenti di sviluppo di assembly side-by-side](side-by-side-assembly-development-tools.md)
</dt> </dl>

 

 



