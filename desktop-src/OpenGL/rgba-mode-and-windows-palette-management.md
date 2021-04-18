---
title: Modalità RGBA e gestione tavolozza Windows
description: Sebbene la maggior parte delle applicazioni GDI tenda a usare l'indicizzazione dei colori con le tavolozze logiche, la modalità RGBA è in genere preferibile per le applicazioni OpenGL. Funziona meglio del mapping dei colori per diversi effetti, ad esempio ombreggiatura, illuminazione, nebbia e mapping di trama.
ms.assetid: 68c35173-e792-4770-9404-5503344f475b
keywords:
- OpenGL in Windows, modalità RGBA
- OpenGL per Windows, gestione tavolozza
- OpenGL in modalità RGBA
- gestione tavolozza OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2e04110d1dfe489a145a8de9bdc7c3d9b726acd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300334"
---
# <a name="rgba-mode-and-windows-palette-management"></a>Modalità RGBA e gestione tavolozza Windows

Sebbene la maggior parte delle applicazioni GDI tenda a usare l'indicizzazione dei colori con le tavolozze logiche, la modalità RGBA è in genere preferibile per le applicazioni OpenGL. Funziona meglio del mapping dei colori per diversi effetti, ad esempio ombreggiatura, illuminazione, nebbia e mapping di trama.

La modalità RGBA usa i valori di colore rosso, verde e blu (R, G e B) che insieme specificano il colore di ogni pixel nella visualizzazione. I valori R, G e B specificano l'intensità di ogni colore (rosso, verde e blu); i valori variano da 0,0 (minimo intenso) a 1,0 (più intenso). Il numero di bit per ogni componente varia a seconda dell'hardware utilizzato (2, 3, 5, 6 e 8 bit possibili). Il colore visualizzato è il risultato della somma dei tre valori di colore. Se tutti e tre i valori sono 0,0, il risultato è nero. Se i tre valori sono tutti 1,0, il risultato è bianco. Altri colori sono il risultato di una combinazione di valori di R, G e B compresi tra 0 e 1,0. Il bit A (Alpha) non viene usato per specificare il colore.

La visualizzazione standard con Super-VGA USA tavolozze con otto bit di colore per pixel. Gli otto bit vengono letti dal buffer e usati come indice nella tavolozza di sistema per ottenere i valori R, G e B. Quando viene selezionata e realizzata una tavolozza RGB in un contesto di dispositivo, è possibile eseguire il rendering di OpenGL usando la modalità RGBA.

Poiché sono presenti otto bit di colore per pixel, OpenGL enfatizza l'uso di una tavolozza RGBA da tre tre due. "Tre-tre-due" indica il modo in cui i dati a colori sono gestiti dalla tavolozza hardware o fisica. I rossi (R) e i verdi (G) sono specificati da tre bit; il blu (B) è specificato da due bit. Il colore rosso è il bit meno significativo e il blu è il bit più significativo.

Si determinano i colori della tavolozza logica dell'applicazione con le strutture [PaletteEntry](/previous-versions//dd162769(v=vs.85)) . In genere si crea una matrice di strutture **PaletteEntry** per specificare l'intera tabella delle voci della tavolozza della tavolozza logica.

## <a name="rgba-mode-palette-sample"></a>Esempio di tavolozza in modalità RGBA

Il frammento di codice seguente mostra come è possibile creare una tavolozza RGBA da tre tre tre due.


```C++
/* 
 * win8map.c - program to create an 8-bit RGB color map for  
 * use with OpenGL 
 * 
 * For OpenGL RGB rendering you need to know red, green, & blue  
 * component bit sizes and positions. On 8 bit palette devices you need  
 * to create a logical palette that has the correct RGBA values for all  
 * 256 possible entries. This program creates an 8 bit RGBA color cube  
 * with a default gamma of 1.4 
 * 
 * Unfortunately, because the standard 20 colors in the system palette  
 * cannot be changed,if you select this palette into an 8-bit display  
 * DC, you will not realize all of the logical palette. The program  
 * changes some of the entries in the logical palette to match enties in  
 * the system palette using a least-squares calculation to find which  
 * entries to replace 
 * 
 * Note: Three bits for red & green and two bits for blue; red is the  
 * least-significant bit and blue is the most-significant bit 
 */ 
 
#include <stdio.h> 
#include <math.h> 
 
#define DEFAULT_GAMMA 1.4F 
 
#define MAX_PAL_ERROR (3*256*256L) 
 
struct colorentry { 
    unsigned char red; 
    unsigned char green; 
    unsigned char blue; 
}; 
 
struct rampentry { 
    struct colorentry color; 
    long defaultindex; 
    unsigned char flags; 
}; 
 
struct defaultentry { 
    struct colorentry color; 
    long rampindex; 
    unsigned char flags; 
}; 
 
/* values for flags */ 
#define EXACTMATCH      0x01 
#define CHANGED         0x02        /* one of the default entries is close */ 
 
/* 
 * These arrays hold bit arrays with a gamma of 1.0  
 * used to convert n bit values to 8-bit values 
 */ 
  
unsigned char threeto8[8] = { 
    0, 0111>>1, 0222>>1, 0333>>1, 0444>>1, 0555>>1, 0666>>1, 0377 
}; 
 
unsigned char twoto8[4] = { 
    0, 0x55, 0xaa, 0xff 
}; 
 
unsigned char oneto8[2] = { 
    0, 255 
}; 
 
struct defaultentry defaultpal[20] = { 
    { 0,   0,   0 }, 
    { 0x80,0,   0 }, 
    { 0,   0x80,0 }, 
    { 0x80,0x80,0 }, 
    { 0,   0,   0x80 }, 
    { 0x80,0,   0x80 }, 
    { 0,   0x80,0x80 }, 
    { 0xC0,0xC0,0xC0 }, 
 
    { 192, 220, 192 }, 
    { 166, 202, 240 }, 
    { 255, 251, 240 }, 
    { 160, 160, 164 }, 
 
    { 0x80,0x80,0x80 }, 
    { 0xFF,0,   0 }, 
    { 0,   0xFF,0 }, 
    { 0xFF,0xFF,0 }, 
    { 0,   0,   0xFF }, 
    { 0xFF,0,   0xFF }, 
    { 0,   0xFF,0xFF }, 
    { 0xFF,0xFF,0xFF } 
}; 
 
struct rampentry rampmap[256]; 
  
void 
gammacorrect(double gamma) 
{ 
    int i; 
    unsigned char v, nv; 
    double dv; 
 
    for (i=0; i<8; i++) { 
        v = threeto8[i]; 
        dv = (255.0 * pow(v/255.0, 1.0/gamma)) + 0.5; 
    nv = (unsigned char)dv; 
    printf("Gamma correct %d to %d (gamma %.2f)\n", v, nv, gamma); 
        threeto8[i] = nv; 
    } 
    for (i=0; i<4; i++) { 
        v = twoto8[i]; 
        dv = (255.0 * pow(v/255.0, 1.0/gamma)) + 0.5; 
    nv = (unsigned char)dv; 
    printf("Gamma correct %d to %d (gamma %.2f)\n", v, nv, gamma); 
        twoto8[i] = nv; 
    } 
    printf("\n"); 
} 
 
main(int argc, char *argv[]) 
{ 
    long i, j, error, min_error; 
    long error_index, delta; 
    double gamma; 
    struct colorentry *pc; 
  
    if (argc == 2) 
        gamma = atof(argv[1]); 
    else 
        gamma = DEFAULT_GAMMA; 
 
    gammacorrect(gamma); 
       
    /* First create a 256 entry RGB color cube */ 
     
    for (i = 0; i < 256; i++) { 
        /* BGR: 2:3:3 */ 
        rampmap[i].color.red = threeto8[(i&7)]; 
        rampmap[i].color.green = threeto8[((i>>3)&7)]; 
        rampmap[i].color.blue = twoto8[(i>>6)&3]; 
    } 
 
    /* Go through the default palette and find exact matches */ 
    for (i=0; i<20; i++) { 
        for(j=0; j<256; j++) { 
            if ( (defaultpal[i].color.red == rampmap[j].color.red) && 
                 (defaultpal[i].color.green == rampmap[j].color.green) && 
                 (defaultpal[i].color.blue == rampmap[j].color.blue)) { 
 
                rampmap[j].flags = EXACTMATCH; 
                rampmap[j].defaultindex = i; 
                defaultpal[i].rampindex = j; 
                defaultpal[i].flags = EXACTMATCH; 
                break; 
            }  
        } 
    } 
 
    /* Now find close matches */             
    for (i=0; i<20; i++) { 
        if (defaultpal[i].flags == EXACTMATCH) 
            continue;         /* skip entries w/ exact matches */ 
        min_error = MAX_PAL_ERROR; 
         
        /* Loop through RGB ramp and calculate least square error */ 
        /* if an entry has already been used, skip it */ 
        for(j=0; j<256; j++) { 
            if (rampmap[j].flags != 0)      /* Already used */ 
                continue; 
                 
            delta = defaultpal[i].color.red - rampmap[j].color.red; 
            error = (delta * delta); 
            delta = defaultpal[i].color.green - rampmap[j].color.green; 
            error += (delta * delta); 
            delta = defaultpal[i].color.blue - rampmap[j].color.blue; 
            error += (delta * delta); 
            if (error < min_error) {        /* New minimum? */ 
                error_index = j; 
                min_error = error; 
            } 
        } 
        defaultpal[i].rampindex = error_index; 
        rampmap[error_index].flags = CHANGED; 
        rampmap[error_index].defaultindex = i; 
    } 
     
    /* First print out the color cube */  
     
    printf("Standard 8-bit RGB color cube with gamma %.2f:\n", gamma); 
    for (i=0; i<256; i++) { 
        pc = &rampmap[i].color;  
        printf("%3ld: (%3-D, %3-D, %3-D)\n", i, pc->red,  
                pc->green, pc->blue); 
     
    } 
    printf("\n"); 
     
    /* Now print out the default entries that have an exact match */ 
 
    for (i=0; i<20; i++) { 
        if (defaultpal[i].flags == EXACTMATCH) { 
            pc = &defaultpal[i].color;  
            printf("Default entry %2ld exactly matched RGB ramp entry  
                      %3ld", i, defaultpal[i].rampindex); 
            printf(" (%3-D, %3-D, %3-D)\n", pc->red, pc->green, pc->blue); 
        } 
    } 
    printf("\n"); 
     
    /* Now print out the closest entries for rest of  
     * the default entries */ 
     
    for (i=0; i<20; i++) { 
        if (defaultpal[i].flags != EXACTMATCH) { 
            pc = &defaultpal[i].color;  
            printf("Default entry %2ld (%3-D, %3-D, %3-D) is close to ", 
                i, pc->red, pc->green, pc->blue); 
            pc = &rampmap[defaultpal[i].rampindex].color; 
            printf("RGB ramp entry %3ld (%3-D, %3-D, %3-D)\n", 
                defaultpal[i].rampindex, pc->red, pc->green, pc->blue); 
        } 
    } 
    printf("\n"); 
     
    /* Print out code to initialize a logical palette  
     * that will not overflow */ 
 
    printf("Here is code you can use to create a logical palette\n"); 
 
    printf("static struct {\n"); 
    printf("    WORD        palVersion;\n"); 
    printf("    WORD        palNumEntries;\n"); 
    printf("    PALETTEENTRY palPalEntries[256];\n"); 
    printf("} rgb8palette = {\n"); 
    printf("    0x300,\n"); 
    printf("    256,\n"); 
 
    for (i=0; i<256; i++) {  
        if (rampmap[i].flags == 0) 
            pc = &rampmap[i].color; 
        else 
            pc = &defaultpal[rampmap[i].defaultindex].color; 
         
        printf("    %3-D, %3-D, %3-D,   0,    /* %ld", 
                pc->red, pc->green, pc->blue, i);  
        if (rampmap[i].flags == EXACTMATCH) 
            printf(" - Exact match with default %d",  
                       rampmap[i].defaultindex); 
        if (rampmap[i].flags == CHANGED) 
            printf(" - Changed to match default %d",  
                       rampmap[i].defaultindex); 
        printf(" */\n"); 
    } 
 
    printf("};\n"); 
    printf("\n    * * *\n\n"); 
    printf("    hpal = CreatePalette((LOGPALETTE *)&rgb8palette);\n"); 
 
    return 0; 
}
```



 

 