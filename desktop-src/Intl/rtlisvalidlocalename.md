---
description: Determina se le impostazioni locali specificate in base al nome sono installate o supportate nel sistema operativo.
ms.assetid: 6df92e4d-d78e-48b5-9515-18f0497de95b
title: Funzione RtlIsValidLocaleName (Ntrtl.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlIsValidLocaleName
api_type:
- DllExport
api_location:
- Kernel32.dll
ms.openlocfilehash: 993d819324987fccdfb66c26343bccfb9a815606655a18ff1a1e43f9a2af0eac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130281"
---
# <a name="rtlisvalidlocalename-function"></a>Funzione RtlIsValidLocaleName

Determina se le impostazioni locali specificate in base al nome sono installate o supportate nel sistema operativo.

> [!Note]  
> Questa funzione è disponibile solo in Windows Vista. Potrebbe essere stato modificato o non disponibile nelle versioni successive. Le applicazioni devono [**usare IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename).

 

## <a name="syntax"></a>Sintassi


```C++
BOOL RtlIsValidLocaleName(
  _In_ LPCWSTR LocaleName,
  _In_ ULONG   Flags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Nome delle impostazioni locali* \[ Pollici\]
</dt> <dd>

[Nome delle impostazioni locali](locale-names.md) da convalidare. Questo parametro può specificare il nome di impostazioni [locali personalizzate.](custom-locales.md)

</dd> <dt>

*Flag* \[ Pollici\]
</dt> <dd>

Flag che indicano se le impostazioni locali non valide sono considerate valide. Attualmente l'unico flag definito è [LOCALE \_ ALLOW \_ NEUTRAL.](locale-allow-neutral.md) Il valore predefinito è che non lo sono.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero in caso di esito positivo oppure 0 in caso contrario.

## <a name="remarks"></a>Commenti

Questa funzione è simile a [**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename). L'unica differenza è che se è impostato LOCALE \_ ALLOW \_ NEUTRAL, **RtlIsValidLocaleName** restituisce **TRUE** per un nome che corrisponde a impostazioni locali neutre (ad esempio "en"), mentre [**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename) restituisce **TRUE** solo per impostazioni locali specifiche (ad esempio "en-US"). Le impostazioni locali neutre vengono usate come parte della strategia di caricamento delle risorse in Windows Vista e versioni successive. Solo una piccola classe di applicazioni altamente specializzate usa **RtlIsValidLocaleName** e imposta LOCALE ALLOW NEUTRAL, perché le impostazioni locali neutre sono \_ di uso molto \_ limitato. Nessuna delle funzioni descritte in [Chiamata delle funzioni "Nome impostazioni locali"](calling-the--locale-name--functions.md) accetta impostazioni locali neutre come input.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Ntrtl.h</dt> </dl>      |
| Libreria<br/>                  | <dl> <dt>Kernel32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Supporto linguistico nazionale](national-language-support.md)
</dt> <dt>

[Funzioni di supporto linguistico nazionale](national-language-support-functions.md)
</dt> <dt>

[**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename)
</dt> </dl>

 

 




