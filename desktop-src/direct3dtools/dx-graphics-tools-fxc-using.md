---
title: Compilazione offline
description: Lo strumento compilatore di effetti (fxc.exe) è progettato per la compilazione offline di shader HLSL.
ms.assetid: 56806335-a0c7-4247-b40d-ba93486a88ac
keywords:
- fxc, compilazione offline
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88a15d3a71dbfb79541a75bd38cb28140d832b45e75a88a52b2d0c8988865f12
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119406331"
---
# <a name="offline-compiling"></a>Compilazione offline

Lo strumento compilatore di effetti (fxc.exe) è progettato per la compilazione offline di shader HLSL.

## <a name="compiling-with-the-current-compiler"></a>Compilazione con il compilatore corrente

I modelli di shader supportati dal compilatore corrente sono visualizzati in [Profili.](dx-graphics-tools-fxc-syntax.md) In questo esempio viene compilato un pixel shader per la destinazione del modello shader 5.1.

```
fxc /T ps_5_1 /Fo PixelShader1.fxc PixelShader1.hlsl
```

Esempio:

-   ps \_ 5 \_ 1 è il profilo di destinazione.
-   PixelShader1.fxc è il file dell'oggetto di output contenente lo shader compilato.
-   PixelShader1.hlsl è l'origine.

```
fxc /Od /Zi /T ps_5_1 /Fo PixelShader1.fxc PixelShader1.hlsl
```

Le opzioni di debug includono opzioni aggiuntive per disabilitare le ottimizzazioni del compilatore (Od) e abilitare le informazioni di debug (Zi), ad esempio i numeri di riga e i simboli.

Per un elenco completo delle opzioni della riga di comando, vedere la [pagina Sintassi.](dx-graphics-tools-fxc-syntax.md)

## <a name="compiling-with-the-legacy-compiler"></a>Compilazione con il compilatore legacy

A partire da Direct3D 10, alcuni modelli di shader non sono più supportati. Sono inclusi pixel shader seguenti: ps \_ \_ 1 1, ps \_ 1 \_ 2, ps \_ 1 3 e ps 1 4 che \_ \_ supportano risorse molto limitate e dipendono \_ dall'hardware. Il compilatore è stato riprogettato con il modello shader 2 (o versione successiva) che consente maggiore efficienza con la compilazione. Ciò richiede naturalmente l'esecuzione su hardware che supporta i modelli di shader 2 e superiori.

Si noti anche che è consigliabile consultare le note sulla versione dell'SDK associate alla versione del compilatore FXC per il comportamento interessato dall'opzione /Gec.

## <a name="using-the-effect-compiler-tool-in-a-subprocess"></a>Uso dello strumento effect-compiler in un sottoprocesso

Se fxc.exe viene generato come sottoprocesso da un'applicazione, è importante assicurarsi che l'applicazione controlli e letta i dati nelle pipe di output o di errore passate alla funzione CreateProcess. Se l'applicazione attende solo il completamento del sottoprocesso e una delle pipe diventa piena, il sottoprocesso non verrà mai completato.

Nell'esempio di codice seguente viene illustrata l'attesa di un sottoprocesso e la lettura delle pipe di output e di errore collegate al sottoprocesso. Il contenuto della matrice corrisponde agli handle per il sottoprocesso, alla pipe per `WaitHandles` stdout e alla pipe per stderr.

```cpp
HANDLE WaitHandles[] = {
  piProcInfo.hProcess, hReadOutPipe, hReadErrorPipe
};

const DWORD BUFSIZE = 4096;
BYTE buff[BUFSIZE];

while (1)
{
    DWORD dwBytesRead, dwBytesAvailable;

    dwWaitResult = WaitForMultipleObjects(3, WaitHandles, FALSE, 60000L);

    // Read from the pipes...
    while (PeekNamedPipe(hReadOutPipe, NULL, 0, NULL, &dwBytesAvailable, NULL) && dwBytesAvailable)
    {
        ReadFile(hReadOutPipe, buff, BUFSIZE - 1, &dwBytesRead, 0);
        streamOut << std::string((char*)buff, (size_t)dwBytesRead);
    }
    while (PeekNamedPipe(hReadErrorPipe, NULL, 0, NULL, &dwBytesAvailable, NULL) && dwBytesAvailable)
    {
        ReadFile(hReadErrorPipe, buff, BUFSIZE - 1, &dwBytesRead, 0);
        streamError << std::string((char*)buff, (size_t)dwBytesRead);
    }

    // Process is done, or we timed out:
    if (dwWaitResult == WAIT_OBJECT_0 || dwWaitResult == WAIT_TIMEOUT)
        break;
}
```

Per altre informazioni sulla generazione di un processo, vedere la pagina di riferimento per [**CreateProcess.**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa)

## <a name="related-topics"></a>Argomenti correlati

* [Strumento compilatore effetti](fxc.md)