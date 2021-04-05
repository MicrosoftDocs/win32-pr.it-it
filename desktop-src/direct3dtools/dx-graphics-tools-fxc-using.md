---
title: Compilazione offline
description: Lo strumento compilatore di effetti (fxc.exe) è progettato per la compilazione offline di shader HLSL.
ms.assetid: 56806335-a0c7-4247-b40d-ba93486a88ac
keywords:
- FXC, compilazione offline
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e7c2bf96a24cb586a5d229a395cbf6dc0cb9ee1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729911"
---
# <a name="offline-compiling"></a>Compilazione offline

Lo strumento compilatore di effetti (fxc.exe) è progettato per la compilazione offline di shader HLSL.

## <a name="compiling-with-the-current-compiler"></a>Compilazione con il compilatore corrente

I modelli shader supportati dal compilatore corrente sono visualizzati nei [profili](dx-graphics-tools-fxc-syntax.md). Questo esempio compila un pixel shader per la destinazione del modello shader 5,1.

```
fxc /T ps_5_1 /Fo PixelShader1.fxc PixelShader1.hlsl
```

In questo esempio:

-   PS \_ 5 \_ 1 è il profilo di destinazione.
-   PixelShader1. fxc è il file oggetto di output contenente lo shader compilato.
-   PixelShader1. HLSL è l'origine.

```
fxc /Od /Zi /T ps_5_1 /Fo PixelShader1.fxc PixelShader1.hlsl
```

Le opzioni di debug includono opzioni aggiuntive per disabilitare le ottimizzazioni del compilatore (od) e abilitare le informazioni di debug (Zi), ad esempio i numeri di riga e i simboli.

Per un elenco completo delle opzioni della riga di comando, vedere la pagina relativa alla [sintassi](dx-graphics-tools-fxc-syntax.md) .

## <a name="compiling-with-the-legacy-compiler"></a>Compilazione con il compilatore legacy

A partire da Direct3D 10, alcuni modelli di shader non sono più supportati. Sono inclusi pixel shader modelli: PS \_ 1 \_ 1, PS \_ 1 \_ 2, PS \_ 1 \_ 3 e PS \_ 1 \_ 4 che supportano risorse molto limitate e che dipendono da hardware. Il compilatore è stato riprogettato con il modello di shader 2 (o versione successiva), che consente una maggiore efficienza con la compilazione. Naturalmente, sarà necessario che l'utente sia in esecuzione su hardware che supporta i modelli shader 2 e versioni successive.

Si noti inoltre che è necessario consultare le note sulla versione dell'SDK associate alla versione del compilatore FXC per il comportamento interessato dall'opzione/GEC.

## <a name="using-the-effect-compiler-tool-in-a-subprocess"></a>Uso dello strumento di compilazione degli effetti in un sottoprocesso

Se fxc.exe viene generato come sottoprocesso da un'applicazione, è importante assicurarsi che l'applicazione controlli e legga tutti i dati nelle pipe di output o di errore passati alla funzione CreateProcess. Se l'applicazione attende solo il completamento del sottoprocesso e una delle pipe diventa completa, il sottoprocesso non viene mai completato.

Nell'esempio di codice seguente viene illustrato l'attesa di un sottoprocesso e la lettura delle pipe di output e di errore associate al sottoprocesso. Il contenuto della `WaitHandles` matrice corrisponde agli handle per il sottoprocesso, alla pipe per stdout e alla pipe per stderr.

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

Per ulteriori informazioni sulla generazione di un processo, vedere la pagina di riferimento per [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa).

## <a name="related-topics"></a>Argomenti correlati

* [Effect-strumento compilatore](fxc.md)