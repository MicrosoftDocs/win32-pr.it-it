---
description: Pktextract.exe è uno strumento che estrae l'attributo publicKeyToken da un file di certificato.
ms.assetid: 195ff5bd-bb60-4053-9308-ceacd29853c0
title: Pktextract.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd163efabd01d65969788aefc2386b2f49079729
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131302"
---
# <a name="pktextractexe"></a>Pktextract.exe

Pktextract.exe è uno strumento che estrae l'attributo **PublicKeyToken** da un file di certificato. L'output è **PublicKeyToken**, ovvero un identificatore univoco a 16 caratteri (8 byte) della chiave pubblica presente nel certificato, in un formato che può essere facilmente incollato in un'istruzione di identità dell'assembly. Il file del certificato deve essere presente nella stessa directory del Pktextract.exe per utilizzare l'utilità. Pktextract.exe è disponibile nel Software Development Kit (SDK) di Microsoft Windows.

## <a name="syntax"></a>Sintassi

**pktextract.exe** *<nomefile. cer>* **\[ -quiet \] \[ -nologo \]**

## <a name="command-line-options"></a>Opzioni da riga di comando

Pktextract.exe usa le seguenti opzioni della riga di comando senza distinzione tra maiuscole e minuscole.



| Opzione  | Descrizione                                                          |
|---------|----------------------------------------------------------------------|
| -quiet  | Evita la visualizzazione completa delle informazioni del certificato. facoltativo.        |
| -nologo | Viene eseguito senza visualizzare i dati di copyright Microsoft standard. facoltativo. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Strumenti di sviluppo di assembly affiancati](side-by-side-assembly-development-tools.md)
</dt> </dl>

 

 



