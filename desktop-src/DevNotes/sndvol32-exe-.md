---
description: Il programma SndVol32.exe controlla le impostazioni del volume per il sistema. Per visualizzare questo controllo volume, passare al pannello di controllo e avviare suoni e dispositivi audio. Passare a volume del dispositivo e fare clic su Avanzate.
ms.assetid: 20e7fb8a-d0a5-46fa-9813-567fa4f57e8f
title: SndVol32.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b24df0f5d6ec25b1843f8aa195c2b365d3f11814
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103965869"
---
# <a name="sndvol32exe"></a>SndVol32.exe

Il programma SndVol32.exe controlla le impostazioni del volume per il sistema. Per visualizzare questo controllo volume, passare al pannello di controllo e avviare suoni e dispositivi audio. Passare a **volume del dispositivo** e fare clic su **Avanzate**.

Per eseguire questo programma con argomenti della riga di comando, andare al menu **Start** , fare clic su **Esegui** e digitare il comando seguente.

**SndVol32.exe \[ -R \| -D** *n * * * \]**

<dl> <dt>

<span id="-R"></span><span id="-r"></span>-R
</dt> <dd>

Avvia l'applicazione in modalità record.

</dd> <dt>

<span id="-D_n"></span><span id="-d_n"></span><span id="-D_N"></span>-D *n*
</dt> <dd>

Specifica un identificatore di dispositivo.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questo programma è il volume audio nativo e il controllo mixer incluso in Windows; non è disponibile per il download da Microsoft. Il programma viene in genere installato nella directory seguente: C: \\ Windows \\ system32.

Per individuare il file nel sistema, aprire Esplora risorse, fare clic sul pulsante **Cerca** e selezionare **tutti i file e le cartelle**. Digitare il nome del file (SndVol32.exe) nella prima riga disponibile e fare clic sul pulsante **Cerca** .

Per ulteriori informazioni sull'utilizzo di questo controllo, avviare il programma e selezionare la **Guida**. Si noti che non è possibile accedere a livello di codice alle funzionalità di questo programma.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[SysTray e SndVol32](https://msdn.microsoft.com/library/ms790410.aspx)
</dt> </dl>

 

 



