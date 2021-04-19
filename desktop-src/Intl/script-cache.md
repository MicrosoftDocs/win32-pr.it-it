---
description: Definisce una cache della metrica del tipo di carattere Uniscribe.
ms.assetid: 56a98529-6ae9-4b71-bd7d-cf056a1e3683
title: SCRIPT_CACHE (usp10. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ece29fe0ed610b4576263c36c50311ef57317579
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317142"
---
# <a name="script_cache"></a>\_cache script

Definisce una cache della metrica del tipo di carattere Uniscribe.


```C++
typedef void* SCRIPT_CACHE;
```



## <a name="remarks"></a>Commenti

Si tratta di una struttura opaca. L'applicazione deve allocare e mantenere una \_ variabile di cache di script per ogni stile di carattere usato. La variabile deve essere inizializzata su **null**.

Molte funzioni di script accettano una combinazione di un handle di contesto di dispositivo hardware e una \_ variabile della cache di script. Uniscribe tenta prima di tutto di accedere ai dati del tipo di carattere tramite la \_ variabile cache script. Controlla solo il contesto del dispositivo hardware se i dati necessari non sono già memorizzati nella cache.

L'handle di contesto del dispositivo hardware può essere passato a Uniscribe come **null**. Se i dati richiesti da Uniscribe sono già memorizzati nella cache, il contesto di dispositivo non è accessibile e l'operazione continua normalmente.

Se il contesto di dispositivo viene passato come **null** e Uniscribe deve accedervi per qualsiasi motivo, Uniscribe restituisce il codice di errore E \_ in sospeso. Questo codice viene restituito rapidamente, consentendo all'applicazione di evitare lunghe chiamate [**SelezionaOggetto**](/windows/win32/api/wingdi/nf-wingdi-selectobject) .

## <a name="examples"></a>Esempio

L'esempio seguente si applica a tutte le funzioni che accettano una \_ variabile della cache script e un handle facoltativo per un contesto di dispositivo hardware.


```C++
hr = ScriptShape(NULL, &sc,
                 pwcChars, cChars, cMaxGlyphs, psa, pwOutGlyphs, pwLogClust, psva, pcGlyphs);
if (hr == E_PENDING)
{
    // ... select font into hdc ...
    hr = ScriptShape(hdc, &sc,
                 pwcChars, cChars, cMaxGlyphs, psa, pwOutGlyphs, pwLogClust, psva, pcGlyphs);
}
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Usp10. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Uniscribe](uniscribe.md)
</dt> <dt>

[Strutture Uniscribe](uniscribe-structures.md)
</dt> <dt>

[Memorizzazione nella cache](caching.md)
</dt> </dl>

 

 
