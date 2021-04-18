---
description: Oltre a essere accessibile tramite l'interfaccia IVssBackupComponents tramite l'oggetto dispositivo della copia, un richiedente può rendere disponibile una copia shadow per altri processi come dispositivo montato in sola lettura.
ms.assetid: 0898c2dc-992a-411b-81df-4f5e129f6a80
title: Esposizione ed emersione di volumi copiati Shadow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d684aa9b696facaf1caa3aa3102c6b1d7fc37409
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318583"
---
# <a name="exposing-and-surfacing-shadow-copied-volumes"></a>Esposizione ed emersione di volumi copiati Shadow

Oltre a essere accessibile tramite l'interfaccia [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) tramite l' [*oggetto dispositivo*](vssgloss-d.md)della copia, un richiedente può rendere disponibile una copia shadow per altri processi come dispositivo montato in sola lettura.

Questo processo è noto come [*esposizione di una copia shadow*](vssgloss-e.md)e viene eseguito usando il metodo [**IVssBackupComponents:: ExposeSnapshot**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-exposesnapshot) .

Una copia shadow può essere esposta come volume locale, a cui è stata assegnata una lettera di unità o associata a una cartella montata, oppure come condivisione file.

Per illustrare, si consideri una copia shadow costituita da un volume nel exposedSys di sistema montato in F: \\ sulla cui radice sono le directory dirOne e dirTwo e il file FileOne.

## <a name="exposing-a-shadow-copy-locally"></a>Esposizione locale di una copia shadow

Quando viene montata come volume locale, la radice della copia shadow è sempre visibile nel punto di montaggio (lettera di unità o cartella montata) e tutti i file copiati dall'ombreggiatura sono visibili.

Se la copia shadow è stata esposta localmente tramite la cartella montata C: \\ ShadowOfF, si troveranno tutti i file presenti sul disco montati a F: \\ al momento della copia shadow disponibile in c: \\ ShadowOfF. L'analisi di C: \\ ShadowOfF potrebbe rivelare due directory, dirOne e dirTwo, e un file, FileOne, in c: \\ ShadowOfF.

Una chiamata a esporre localmente la copia shadow potrebbe essere:

``` syntax
  IVssBackupComponents *pReq;
  VSS_ID snapID;
  PWSTR wszExposed;
  //    .
  //    .
  hr = pReg->ExposeSnapshot(
         snapID,                           // VSS_ID SnapshotId,
         NULL,                             // VSS_PWSZ wszPathFromRoot
         VSS_VOLSNAP_ATTR_EXPOSED_LOCALLY, // LONG lAttributes
         L"C:\ShadowOfF",                  // VSS_PWSZ wszExpose
         LPWSTR &wszExposed,               // VSS_PWSZ* pwszExposed
       );
```

Se la copia shadow è stata esposta correttamente localmente, *wszExposed* deve contenere la stringa di caratteri wide "C: \\ ShadowOfF".

In seguito, la copia shadow può essere non esposta chiamando [**IVssBackupComponentsEx2:: UnexposeSnapshot**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-unexposesnapshot).

Solo le copie shadow persistenti, ovvero le copie shadow create con il rollback dell' \_ app VSS CTX \_ NAS \_ o VSS \_ ctx, \_ \_ possono essere esposte localmente.

## <a name="exposing-a-shadow-copy-as-a-remote-share"></a>Esposizione di una copia shadow come condivisione remota

In alternativa, è possibile scegliere di rendere la copia shadow del disco montata in F: \\ disponibile come condivisione file remota ed esporre solo i dati in dirTwo come condivisione file dirTwoOfF.

In questo caso, i sistemi possono accedere alla copia shadow dei file in F: \\ dirTwo eseguendo il mapping di \\ \\ exposedSys \\ dirTwoOfF come unità di rete.

Una chiamata a implement Remote esponendo la copia shadow come condivisione potrebbe essere la seguente:

``` syntax
  IVssBackupComponents *pReq;
  VSS_ID snapID;
  LPWSTR wszExposed;
  //    .
  //    .
  hr = pReg->ExposeSnapshot(
               snapID,                            // VSS_ID SnapshotId,
               L"\dirTwo",                        // VSS_PWSZ wszPathFromRoot
               VSS_VOLSNAP_ATTR_EXPOSED_REMOTELY, // LONG lAttributes
               L"dirTwoOfF",                      // VSS_PWSZ wszExpose
               LPWSTR &wszExposed,                // VSS_PWSZ* pwszExposed
       );
```

Se la copia shadow è stata esposta in remoto, *wszExposed* deve contenere la stringa di caratteri wide "dirTwoOfF".

Qualsiasi sistema che attualmente sta eseguendo il mapping della condivisione di rete di dirTwoOfF potrebbe disconnettersi, così come potrebbe disconnettersi da qualsiasi condivisione ordinaria.

## <a name="surfacing-a-shadow-copy"></a>Emersione di una copia shadow

Una [*copia shadow di superficie*](vssgloss-s.md) è una copia in cui la copia shadow è nota allo spazio dei nomi del gestore di montaggio di un sistema.

Ciò significa che è possibile individuare tali copie shadow in modo analogo a qualsiasi altro volume disponibile ma non ancora montato, ad esempio usando **FindFirstVolume** e **FindNextVolume**.

Ovviamente, le copie shadow esposte sono anche copie shadow di superficie. Tuttavia, il contrario non è necessariamente vero.

Se una copia shadow esposta localmente è stata smontata o un sistema ha scelto di disconnettere una copia shadow esposta in modalità remota, la copia shadow non verrà più esposta. Tuttavia, finché la copia shadow viene mantenute, i volumi verrebbero esposti. Ciò significa che possono essere montati come qualsiasi altro volume di sola lettura.

 

 



