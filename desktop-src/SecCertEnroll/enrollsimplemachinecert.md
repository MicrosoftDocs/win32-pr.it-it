---
description: Registra un computer in una gerarchia di certificati usando un modello, un nome visualizzato del certificato e la descrizione del certificato.
ms.assetid: d9e01767-f6e8-4fd6-a848-8d5acf57407e
title: enrollSimpleMachineCert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb533dc2c0d262a64f8fd1d2245c310880586c04900ef028e7c2609f1a6b4577
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119976901"
---
# <a name="enrollsimplemachinecert"></a>enrollSimpleMachineCert

L'esempio enrollSimpleMachineCert registra un computer in una gerarchia di certificati usando un modello, un nome visualizzato del certificato e la descrizione del certificato.

## <a name="location"></a>Località

Quando si installa Microsoft Windows Software Development Kit (SDK), per impostazione predefinita viene installata una versione C++ dell'esempio nella cartella *%ProgramFiles%* \\ Microsoft SDKs \\ Windows \\ v7.0 \\ Samples Security \\ \\ X509 Certificate Enrollment \\ VC \\ EnrollSimpleMachineCert. Una versione di VBScript viene installata nella cartella *%ProgramFiles%* \\ Microsoft SDKs \\ Windows \\ v7.0 \\ Samples Security \\ \\ X509 Certificate Enrollment \\ VBS \\ EnrollSimpleMachineCert .

## <a name="discussion"></a>Discussione

L'esempio enrollSimpleMachineCert:

1.  Elabora gli argomenti della riga di comando. La riga di comando deve contenere il nome del modello, un nome visualizzato del certificato e una descrizione del certificato.
2.  Crea un [**oggetto IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) e lo inizializza usando il modello specificato nella riga di comando. Il valore ContextAdministratorForceMachine per il primo parametro specifica che il certificato viene richiesto da un amministratore che agisce per conto di un computer.
3.  Aggiunge il nome visualizzato e la descrizione all'oggetto registrazione.
4.  Tenta di registrare la richiesta di certificato e controlla lo stato del processo. La funzione checkEnrollStatus è definita in enrollCommon.cpp.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso degli esempi inclusi](using-the-included-samples.md)
</dt> </dl>

 

 



