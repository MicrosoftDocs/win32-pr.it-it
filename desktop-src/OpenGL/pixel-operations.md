---
title: Operazioni pixel
description: Operazioni pixel
ms.assetid: e60cc45b-867c-441a-b579-8c7dbd46ecd9
keywords:
- Operazioni pixel OpenGL
topic_type:
- apiref
api_name:
- Pixel Operations
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fda15342b246ba979bdbe60184eeb632368f36b4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103857274"
---
# <a name="pixel-operations"></a>Operazioni pixel

<dl> <dt><span id="GL_SCISSOR_TEST"></span><span id="gl_scissor_test"></span>\_test della forbice GL \_</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Descrizione:     | Scissoring abilitato                 |
| Gruppo di attributi: | Scissor/Enable                     |
| Valore iniziale:   | GL \_ false                          |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_SCISSOR_BOX"></span><span id="gl_scissor_box"></span>\_casella della forbice GL \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | Casella Scissor                                                                      |
| Gruppo di attributi: | ritaglio                                                                          |
| Valore iniziale:   |                                                                                  |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_STENCIL_TEST"></span><span id="gl_stencil_test"></span>\_test stencil \_ GL</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Descrizione:     | Stencil abilitato                 |
| Gruppo di attributi: | stencil-buffer/Abilita              |
| Valore iniziale:   | GL \_ false                          |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_STENCIL_FUNC"></span><span id="gl_stencil_func"></span>funzione \_ stencil \_ GL</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | Funzione stencil                                                                 |
| Gruppo di attributi: | stencil-buffer                                                                   |
| Valore iniziale:   | GL \_ Always                                                                       |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_STENCIL_VALUE_MASK"></span><span id="gl_stencil_value_mask"></span>\_maschera del \_ valore dello stencil GL \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | Maschera stencil                                                                     |
| Gruppo di attributi: | stencil-buffer                                                                   |
| Valore iniziale:   | 1                                                                              |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_STENCIL_REF"></span><span id="gl_stencil_ref"></span>\_riferimento allo stencil GL \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | Valore riferimento stencil                                                          |
| Gruppo di attributi: | stencil-buffer                                                                   |
| Valore iniziale:   | 0                                                                                |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_STENCIL_FAIL"></span><span id="gl_stencil_fail"></span>\_stencil GL \_ non riuscito</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | Azione di errore stencil                                                              |
| Gruppo di attributi: | stencil-buffer                                                                   |
| Valore iniziale:   | \_conservazione GL                                                                         |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_STENCIL_PASS_DEPTH_FAIL"></span><span id="gl_stencil_pass_depth_fail"></span>\_errore di \_ profondità del passaggio dello stencil GL \_ \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | Azione errore buffer profondità stencil                                                 |
| Gruppo di attributi: | stencil-buffer                                                                   |
| Valore iniziale:   | \_conservazione GL                                                                         |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_STENCIL_PASS_DEPTH_PASS"></span><span id="gl_stencil_pass_depth_pass"></span>\_passaggio di \_ profondità del passaggio dello stencil GL \_ \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | Azione passaggio buffer profondità stencil                                                 |
| Gruppo di attributi: | stencil-buffer                                                                   |
| Valore iniziale:   | \_conservazione GL                                                                         |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_ALPHA_TEST"></span><span id="gl_alpha_test"></span>\_test GL Alpha \_</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Descrizione:     | Test alfa abilitato                 |
| Gruppo di attributi: | colore-buffer/Abilita                |
| Valore iniziale:   | GL \_ false                          |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_ALPHA_TEST_FUNC"></span><span id="gl_alpha_test_func"></span>funzione \_ di \_ test GL Alpha \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | Funzione di test Alpha                                                              |
| Gruppo di attributi: | buffer a colori                                                                     |
| Valore iniziale:   | GL \_ Always                                                                       |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_ALPHA_TEST_REF"></span><span id="gl_alpha_test_ref"></span>\_ref del \_ test GL Alpha \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | Valore di riferimento del test alfa                                                       |
| Gruppo di attributi: | buffer a colori                                                                     |
| Valore iniziale:   | 0                                                                                |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_DEPTH_TEST"></span><span id="gl_depth_test"></span>\_test di profondità GL \_</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Descrizione:     | Buffer di profondità abilitato               |
| Gruppo di attributi: | depth-buffer/Enable                |
| Valore iniziale:   | GL \_ false                          |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_DEPTH_FUNC"></span><span id="gl_depth_func"></span>funzione di \_ profondità GL \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | Funzione di test del buffer di profondità                                                       |
| Gruppo di attributi: | buffer di profondità                                                                     |
| Valore iniziale:   | \_meno GL                                                                         |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_BLEND"></span><span id="gl_blend"></span>\_Blend GL</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Descrizione:     | Blending abilitato                   |
| Gruppo di attributi: | colore-buffer/Abilita                |
| Valore iniziale:   | GL \_ false                          |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_BLENC_SRC"></span><span id="gl_blenc_src"></span>\_src BLENC \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | Funzione di origine blending                                                         |
| Gruppo di attributi: | buffer a colori                                                                     |
| Valore iniziale:   | GL \_ uno                                                                          |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_BLEND_DST"></span><span id="gl_blend_dst"></span>\_DST Blend \_ DST</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | Funzione di destinazione di Blend                                                    |
| Gruppo di attributi: | buffer a colori                                                                     |
| Valore iniziale:   | \_zero GL                                                                         |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_DITHER"></span><span id="gl_dither"></span>\_dithering GL</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Descrizione:     | Rethering abilitato                  |
| Gruppo di attributi: | colore-buffer/Abilita                |
| Valore iniziale:   | GL \_ true                           |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_LOGIC_OP"></span><span id="gl_logic_op"></span>\_op logica \_ GL</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Descrizione:     | Operazione logica abilitata          |
| Gruppo di attributi: | colore-buffer/Abilita                |
| Valore iniziale:   | GL \_ false                          |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_LOGIC_OP_MODE"></span><span id="gl_logic_op_mode"></span>\_ \_ modalità operativa logica \_ GL</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descrizione:     | Funzione logica Operation                                                       |
| Gruppo di attributi: | buffer a colori                                                                     |
| Valore iniziale:   | \_copia GL                                                                         |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> </dl>

 

 




