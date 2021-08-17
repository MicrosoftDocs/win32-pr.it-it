---
description: NLS include una serie di funzioni API che le applicazioni possono usare per eseguire il mapping dei dati delle impostazioni locali tra gli identificatori delle impostazioni locali e i nomi delle impostazioni locali ed elencare le impostazioni locali neutre.
ms.assetid: 01bc261d-dfee-430e-86c9-cfafe82856c8
title: Mapping dei dati delle impostazioni locali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1576844f13dda80a6b9d754fc807ef8a35514dcfedd88dc04cf233cfb2a1bfb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147193"
---
# <a name="mapping-locale-data"></a>Mapping dei dati delle impostazioni locali

NLS include una serie di funzioni API che le [](locale-identifiers.md) applicazioni possono usare per eseguire il mapping dei dati delle impostazioni locali tra gli identificatori delle impostazioni locali e i nomi delle impostazioni locali [ed](locale-names.md)elencare le impostazioni locali neutre. Questo argomento illustra l'uso di queste funzioni in Windows Vista e versioni successive e nei sistemi operativi Windows Vista pre-Windows (talvolta denominati "sistemi di livello inferiore").

## <a name="map-locale-data-on-windows-vista-and-later"></a>Eseguire il mapping dei dati delle impostazioni locali Windows Vista e versioni successive

NLS offre diverse funzioni di mapping delle impostazioni locali per l'uso da parte delle applicazioni sviluppate per l'esecuzione Windows Vista e versioni successive. Include anche funzioni che le applicazioni possono usare per enumerare le impostazioni locali neutre.

**Usare le funzioni di conversione standard per il mapping dei dati**

Per eseguire il mapping tra un nome delle impostazioni locali e un identificatore delle impostazioni locali, l'applicazione può chiamare la [**funzione LocaleNameToLCID.**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) L'applicazione usa [**LCIDToLocaleName per**](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename) eseguire il mapping tra un identificatore delle impostazioni locali e un nome delle impostazioni locali.

**Elencare le impostazioni locali neutre**

Per enumerare le impostazioni locali neutre Windows 7 e versioni successive, l'applicazione può chiamare [**EnumSystemLocalesEx**](/windows/desktop/api/Winnls/nf-winnls-enumsystemlocalesex) con *dwFlags* impostato su [**LOCALE \_ NEUTRALDATA.**](locale-neutraldata.md) Può anche usare [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) con *LCType* impostato su [**LOCALE \_ INEUTRAL.**](locale-ineutral.md)

## <a name="map-locale-data-on-pre-windows-vista-operating-systems"></a>Eseguire il mapping dei dati delle impostazioni locali nei sistemi operativi Windows Vista

NLS include una libreria a collegamento diretto (DLL) da usare per le applicazioni sviluppate per l'esecuzione nei sistemi operativi Windows Vista. La DLL supporta funzioni di conversione ed elenco per il mapping dei dati.

> [!Note]  
> Le applicazioni eseguite solo in Windows Vista e versioni successive non devono usare le funzioni di mapping o elenco di livello inferiore.

 

**Usare le funzioni di conversione di livello inferiore per il mapping dei dati**

L'applicazione destinata a un sistema di livello inferiore può chiamare la [**funzione DownlevelLCIDToLocaleName**](downlevellcidtolocalename.md) per convertire un identificatore delle impostazioni locali in un nome di impostazioni locali. Se è necessario convertire un nome delle impostazioni locali in un identificatore delle impostazioni locali, deve chiamare [**DownlevelLocaleNameToLCID**](downlevellocalenametolcid.md).

**Usare le funzioni di elenco di livello inferiore per enumerare le impostazioni locali neutre**

L'applicazione deve chiamare [**DownlevelGetParentLocaleLCID**](downlevelgetparentlocalelcid.md) per recuperare l'identificatore delle impostazioni locali dell'elemento padre per le impostazioni locali. Se l'applicazione deve ottenere il nome delle impostazioni locali dell'elemento padre per le impostazioni locali, deve chiamare [**DownlevelGetParentLocaleName**](downlevelgetparentlocalename.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso del supporto linguistico nazionale](using-national-language-support.md)
</dt> <dt>

[Identificatori delle impostazioni locali](locale-identifiers.md)
</dt> <dt>

[Nomi delle impostazioni locali](locale-names.md)
</dt> </dl>

 

 



